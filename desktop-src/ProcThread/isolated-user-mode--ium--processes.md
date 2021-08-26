---
description: Windows 10 una nueva característica de seguridad denominada Modo seguro virtual (VSM).
ms.assetid: 58374CC4-593F-4B91-A5E4-85E29C44F8B4
title: Procesos de modo de usuario aislado (IUM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 982d9924f60d02a74aa7237e5c3bb16e787f1d3a0cc07e9693e9cd47335cedc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032554"
---
# <a name="isolated-user-mode-ium-processes"></a>Procesos de modo de usuario aislado (IUM)

Windows 10 una nueva característica de seguridad denominada Modo seguro virtual (VSM). VSM aprovecha el hipervisor de Hyper-V y la traducción de direcciones de segundo nivel (SLAT) para crear un conjunto de modos denominados Niveles de confianza virtual (VTL). Esta nueva arquitectura de software crea un límite de seguridad para evitar que los procesos que se ejecutan en un VTL accedan a la memoria de otra VTL. La ventaja de este aislamiento incluye la mitigación adicional de vulnerabilidades de kernel al proteger recursos como hash de contraseña y claves Kerberos.

En el diagrama 1 se muestra el modelo tradicional del modo kernel y el código de modo de usuario que se ejecuta en los anillos de CPU 0 y 3, respectivamente. En este nuevo modelo, el código que se ejecuta en el modelo tradicional se ejecuta en VTL0 y no puede acceder al VTL1 con privilegios más altos, donde el kernel seguro y el modo de usuario aislado (IUM) ejecutan código. Las VTL son jerárquicos, lo que significa que cualquier código que se ejecuta en VTL1 tiene más privilegios que el código que se ejecuta en VTL0.

El aislamiento de VTL lo crea el hipervisor de Hyper-V, que asigna memoria en tiempo de arranque mediante la traducción de direcciones de segundo nivel (SLAT). Continúa de forma dinámica a medida que se ejecuta el sistema, protegiendo la memoria que el kernel seguro especifica que necesita protección de VTL0, ya que se usará para contener secretos. Como se asignan bloques de memoria independientes para las dos VTL, se crea un entorno de tiempo de ejecución seguro para VTL1 mediante la asignación de bloques de memoria exclusivos a VTL1 y VTL0 con los permisos de acceso adecuados.

**Diagrama 1: Arquitectura de IUM**

![diagrama 1: arquitectura de ium](images/uim-architecture.png)

## <a name="trustlets"></a>Trustlets

Los trustlets (también conocidos como procesos de confianza, procesos seguros o procesos IUM) son programas que se ejecutan como procesos de IUM en VSM. Para completar las llamadas del sistema, se pueden Windows en el kernel que se ejecuta en el anillo VTL0 0. VSM crea un entorno de ejecución pequeño que incluye el pequeño kernel seguro que se ejecuta en VTL1 (aislado del kernel y los controladores que se ejecutan en VTL0). La ventaja de seguridad clara es el aislamiento de las páginas de modo de usuario trustlet en VTL1 de los controladores que se ejecutan en el kernel VTL0. Incluso si el modo kernel de VTL0 está en peligro por malware, no tendrá acceso a las páginas de proceso de IUM.

Con VSM habilitado, el entorno de autoridad de seguridad local (LSASS) se ejecuta como trustlet. LSASS administra la directiva del sistema local, la autenticación de usuarios y la auditoría mientras se administran datos de seguridad confidenciales, como hash de contraseña y claves Kerberos. Para aprovechar las ventajas de seguridad de VSM, un trustlet denominado LSAISO.exe (LSA aislado) se ejecuta en VTL1 y se comunica con LSASS.exe que se ejecuta en VTL0 a través de un canal RPC. Los secretos LSAISO se cifran antes de enviarlos a LSASS que se ejecuta en modo normal de VSM y las páginas de LSAISO están protegidas contra código malintencionado que se ejecuta en VTL0.

**Diagrama 2: Diseño de trustlet de LSASS**

![diagrama 2: diseño de trustlet lsass ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a>Implicaciones del modo de usuario aislado (IUM)

No es posible adjuntar a un proceso de IUM, lo que impide la capacidad de depurar código VTL1. Esto incluye la depuración post-mortem de volcados de memoria y la asociación de las herramientas de depuración para la depuración en vivo. También incluye intentos de cuentas con privilegios o controladores de kernel para cargar un archivo DLL en un proceso de IUM, insertar un subproceso o entregar un APC en modo de usuario. Estos intentos pueden dar lugar a la desestabilización de todo el sistema. Windows Las API que podrían poner en peligro la seguridad de un trustlet pueden producir errores de maneras inesperadas. Por ejemplo, la carga de un archivo DLL en un trustlet hará que esté disponible en VTL0, pero no en VTL1. QueueUserApc puede producir un error en modo silencioso si el subproceso de destino está en un Trustlet. Otras API, como CreateRemoteThread, VirtualAllocEx y Read/WriteProcessMemory tampoco funcionarán según lo previsto cuando se utilicen en trustlets.

Use el código de ejemplo siguiente para evitar llamar a cualquier función que intente adjuntar o insertar código en un proceso de IUM. Esto incluye los controladores de kernel que ponen en cola las API para la ejecución del código en un trustlet.

## <a name="remarks"></a>Comentarios

Si el estado devuelto de IsSecureProcess es correcto, examine el parámetro SecureProcess Out para determinar si el proceso \_ \_ es un proceso IUM. El sistema marca los procesos IUM como "Procesos seguros". Un resultado booleano de TRUE significa que el proceso de destino es de tipo IUM.


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



WdK for Windows 10, "Windows Driver Kit - Windows 10.0.15063.0", contiene la definición necesaria de la estructura PROCESS \_ EXTENDED \_ BASIC \_ INFORMATION. La versión actualizada de la estructura se define en ntddk.h con el nuevo campo IsSecureProcess.


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



 

 



