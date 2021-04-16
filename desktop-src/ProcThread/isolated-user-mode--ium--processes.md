---
description: Windows 10 presentó una nueva característica de seguridad denominada modo seguro virtual (VSM).
ms.assetid: 58374CC4-593F-4B91-A5E4-85E29C44F8B4
title: Procesos de modo de usuario aislado (IUM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a176421174a58abe4ab595bb37ab75434edade
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104570792"
---
# <a name="isolated-user-mode-ium-processes"></a>Procesos de modo de usuario aislado (IUM)

Windows 10 presentó una nueva característica de seguridad denominada modo seguro virtual (VSM). VSM aprovecha el hipervisor de Hyper-V y la traducción de direcciones de segundo nivel (SLAT) para crear un conjunto de modos denominados niveles de confianza virtual (VTLs). Esta nueva arquitectura de software crea un límite de seguridad para evitar que los procesos que se ejecutan en una VTL accedan a la memoria de otra VTL. La ventaja de este aislamiento incluye la mitigación adicional de las vulnerabilidades de seguridad del kernel y la protección de los recursos, como los hash de contraseñas y las claves de Kerberos.

En el diagrama 1 se describe el modelo tradicional de modo kernel y el código de modo de usuario que se ejecuta en el anillo de CPU 0 y anillo 3, respectivamente. En este nuevo modelo, el código que se ejecuta en el modelo tradicional se ejecuta en VTL0 y no puede tener acceso al VTL1 con privilegios elevados, donde el kernel seguro y el modo de usuario aislado (IUM) ejecutan código. Las VTLs son jerárquicas, lo que significa que cualquier código que se ejecute en VTL1 tiene más privilegios que el código que se ejecuta en VTL0.

El hipervisor de Hyper-V crea el aislamiento de VTL, que asigna memoria durante el arranque con la traducción de direcciones de segundo nivel (SLAT). Continúa esto de forma dinámica a medida que se ejecuta el sistema y protege la memoria. el kernel seguro especifica la necesidad de protección de VTL0 porque se usará para contener secretos. A medida que se asignan bloques de memoria independientes para las dos VTLs, se crea un entorno de tiempo de ejecución seguro para VTL1 mediante la asignación de bloques de memoria exclusivos a VTL1 y VTL0 con los permisos de acceso adecuados.

**Diagrama 1: arquitectura de IUM**

![Diagrama 1: arquitectura de Ium](images/uim-architecture.png)

## <a name="trustlets"></a>Trustlets

Trustlets (también conocido como procesos de confianza, procesos seguros o procesos IUM) son programas que se ejecutan como procesos de IUM en VSM. Completan las llamadas del sistema mediante su cálculo de referencias en el kernel de Windows que se ejecuta en VTL0 Ring 0. VSM crea un pequeño entorno de ejecución que incluye el pequeño kernel seguro que se ejecuta en VTL1 (aislado del kernel y los controladores que se ejecutan en VTL0). La ventaja de seguridad clara es el aislamiento de las páginas del modo de usuario de trustlet de VTL1 de los controladores que se ejecutan en el kernel VTL0. Aunque el modo kernel de VTL0 esté en peligro por malware, no tendrá acceso a las páginas de proceso de IUM.

Con VSM habilitado, el entorno de la autoridad de seguridad local (LSASS) se ejecuta como trustlet. LSASS administra la Directiva del sistema local, la autenticación de usuarios y la auditoría mientras se manejan los datos de seguridad confidenciales, como los hash de contraseña y las claves de Kerberos. Para aprovechar las ventajas de seguridad de VSM, un trustlet con nombre LSAISO.exe (LSA aislado) se ejecuta en VTL1 y se comunica con LSASS.exe que se ejecutan en VTL0 a través de un canal de RPC. Los secretos de LSAISO se cifran antes de enviarlos a LSASS que se ejecutan en modo de VSM normal y las páginas de LSAISO están protegidas frente a código malintencionado que se ejecuta en VTL0.

**Diagrama 2: diseño de Trustlet de LSASS**

![Diagrama 2: diseño de trustlet de LSASS ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a>Implicaciones del modo de usuario aislado (IUM)

No es posible asociar a un proceso de IUM, lo que impide la capacidad de depurar el código de VTL1. Esto incluye la depuración posterior a mortem de volcados de memoria y la Asociación de las herramientas de depuración para la depuración en directo. También incluye los intentos de los controladores de kernel o las cuentas con privilegios para cargar un archivo DLL en un proceso de IUM, para inyectar un subproceso o para proporcionar un APC en modo de usuario. Estos intentos pueden dar lugar a la desestabilización de todo el sistema. Las API de Windows que podrían poner en peligro la seguridad de un Trustlet podrían producir errores inesperados. Por ejemplo, la carga de un archivo DLL en un Trustlet lo hará disponible en VTL0, pero no VTL1. QueueUserApc puede producir un error en modo silencioso si el subproceso de destino está en un Trustlet. Otras API, como CreateRemoteThread, VirtualAllocEx y Read/WriteProcessMemory tampoco funcionarán de la manera esperada cuando se usan en Trustlets.

Use el código de ejemplo siguiente para evitar la llamada a cualquier función que intente adjuntar o insertar código en un proceso de IUM. Esto incluye los controladores de kernel que ponen en cola APC para la ejecución de código en un trustlet.

## <a name="remarks"></a>Observaciones

Si el estado de retorno de IsSecureProcess es Success, examine el \_ parámetro out de SecureProcess \_ para determinar si el proceso es un proceso de Ium. Los procesos de IUM están marcados por el sistema para ser "procesos seguros". Un resultado booleano de TRUE significa que el proceso de destino es de tipo IUM.


```C++
NTSTATUS
IsSecureProcess(
   _In_ HANDLE ProcessHandle,
   _Out_ BOOLEAN *SecureProcess
   )
{
   NTSTATUS status;

       // definition included in ntddk.h  
   PROCESS_EXTENDED_BASIC_INFORMATION extendedInfo = {0};
 
   PAGED_CODE(); 
  
   extendedInfo.Size = sizeof(extendedInfo);

   // Query for the process information  
   status = ZwQueryInformationProcess(
                  ProcessHandle, ProcessBasicInformation, &extendedInfo,
                  sizeof(extendedInfo), NULL);

   if (NT_SUCCESS(status)) {
      *SecureProcess = (BOOLEAN)(extendedInfo.IsSecureProcess != 0);
   }
 
          return status;
}
```



WDK para Windows 10, "Windows Driver Kit-Windows 10.0.15063.0", contiene la definición necesaria de la estructura de \_ la \_ información básica extendida del proceso \_ . La versión actualizada de la estructura se define en ntddk. h con el nuevo campo IsSecureProcess.


```C++
typedef struct _PROCESS_EXTENDED_BASIC_INFORMATION {
    SIZE_T Size;    // Ignored as input, written with structure size on output
    PROCESS_BASIC_INFORMATION BasicInfo;
    union {
        ULONG Flags;
        struct {
            ULONG IsProtectedProcess : 1;
            ULONG IsWow64Process : 1;
            ULONG IsProcessDeleting : 1;
            ULONG IsCrossSessionCreate : 1;
            ULONG IsFrozen : 1;
            ULONG IsBackground : 1;
            ULONG IsStronglyNamed : 1;
            ULONG IsSecureProcess : 1;
            ULONG IsSubsystemProcess : 1;
            ULONG SpareBits : 23;
        } DUMMYSTRUCTNAME;
    } DUMMYUNIONNAME;
} PROCESS_EXTENDED_BASIC_INFORMATION, *PPROCESS_EXTENDED_BASIC_INFORMATION;
```



 

 



