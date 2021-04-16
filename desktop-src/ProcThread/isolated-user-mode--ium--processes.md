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
# <a name="isolated-user-mode-ium-processes"></a><span data-ttu-id="31100-103">Procesos de modo de usuario aislado (IUM)</span><span class="sxs-lookup"><span data-stu-id="31100-103">Isolated User Mode (IUM) Processes</span></span>

<span data-ttu-id="31100-104">Windows 10 presentó una nueva característica de seguridad denominada modo seguro virtual (VSM).</span><span class="sxs-lookup"><span data-stu-id="31100-104">Windows 10 introduced a new security feature named Virtual Secure Mode (VSM).</span></span> <span data-ttu-id="31100-105">VSM aprovecha el hipervisor de Hyper-V y la traducción de direcciones de segundo nivel (SLAT) para crear un conjunto de modos denominados niveles de confianza virtual (VTLs).</span><span class="sxs-lookup"><span data-stu-id="31100-105">VSM leverages the Hyper-V Hypervisor and Second Level Address Translation (SLAT) to create a set of modes called Virtual Trust Levels (VTLs).</span></span> <span data-ttu-id="31100-106">Esta nueva arquitectura de software crea un límite de seguridad para evitar que los procesos que se ejecutan en una VTL accedan a la memoria de otra VTL.</span><span class="sxs-lookup"><span data-stu-id="31100-106">This new software architecture creates a security boundary to prevent processes running in one VTL from accessing the memory of another VTL.</span></span> <span data-ttu-id="31100-107">La ventaja de este aislamiento incluye la mitigación adicional de las vulnerabilidades de seguridad del kernel y la protección de los recursos, como los hash de contraseñas y las claves de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="31100-107">The benefit of this isolation includes additional mitigation from kernel exploits while protecting assets such as password hashes and Kerberos keys.</span></span>

<span data-ttu-id="31100-108">En el diagrama 1 se describe el modelo tradicional de modo kernel y el código de modo de usuario que se ejecuta en el anillo de CPU 0 y anillo 3, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="31100-108">Diagram 1 depicts the traditional model of Kernel mode and User mode code running in CPU ring 0 and ring 3, respectively.</span></span> <span data-ttu-id="31100-109">En este nuevo modelo, el código que se ejecuta en el modelo tradicional se ejecuta en VTL0 y no puede tener acceso al VTL1 con privilegios elevados, donde el kernel seguro y el modo de usuario aislado (IUM) ejecutan código.</span><span class="sxs-lookup"><span data-stu-id="31100-109">In this new model, the code running in the traditional model executes in VTL0 and it cannot access the higher privileged VTL1, where the Secure Kernel and Isolated User Mode (IUM) execute code.</span></span> <span data-ttu-id="31100-110">Las VTLs son jerárquicas, lo que significa que cualquier código que se ejecute en VTL1 tiene más privilegios que el código que se ejecuta en VTL0.</span><span class="sxs-lookup"><span data-stu-id="31100-110">The VTLs are hierarchal meaning any code running in VTL1 is more privileged than code running in VTL0.</span></span>

<span data-ttu-id="31100-111">El hipervisor de Hyper-V crea el aislamiento de VTL, que asigna memoria durante el arranque con la traducción de direcciones de segundo nivel (SLAT).</span><span class="sxs-lookup"><span data-stu-id="31100-111">The VTL isolation is created by the Hyper-V Hypervisor which assigns memory at boot time using Second Level Address Translation (SLAT).</span></span> <span data-ttu-id="31100-112">Continúa esto de forma dinámica a medida que se ejecuta el sistema y protege la memoria. el kernel seguro especifica la necesidad de protección de VTL0 porque se usará para contener secretos.</span><span class="sxs-lookup"><span data-stu-id="31100-112">It continues this dynamically as the system runs, protecting memory the Secure Kernel specifies needing protection from VTL0 because it will be used to contain secrets.</span></span> <span data-ttu-id="31100-113">A medida que se asignan bloques de memoria independientes para las dos VTLs, se crea un entorno de tiempo de ejecución seguro para VTL1 mediante la asignación de bloques de memoria exclusivos a VTL1 y VTL0 con los permisos de acceso adecuados.</span><span class="sxs-lookup"><span data-stu-id="31100-113">As separate blocks of memory are allocated for the two VTLs, a secure runtime environment is created for VTL1 by assigning exclusive memory blocks to VTL1 and VTL0 with the appropriate access permissions.</span></span>

<span data-ttu-id="31100-114">**Diagrama 1: arquitectura de IUM**</span><span class="sxs-lookup"><span data-stu-id="31100-114">**Diagram 1 - IUM Architecture**</span></span>

![Diagrama 1: arquitectura de Ium](images/uim-architecture.png)

## <a name="trustlets"></a><span data-ttu-id="31100-116">Trustlets</span><span class="sxs-lookup"><span data-stu-id="31100-116">Trustlets</span></span>

<span data-ttu-id="31100-117">Trustlets (también conocido como procesos de confianza, procesos seguros o procesos IUM) son programas que se ejecutan como procesos de IUM en VSM.</span><span class="sxs-lookup"><span data-stu-id="31100-117">Trustlets (also known as trusted processes, secure processes, or IUM processes) are programs running as IUM processes in VSM.</span></span> <span data-ttu-id="31100-118">Completan las llamadas del sistema mediante su cálculo de referencias en el kernel de Windows que se ejecuta en VTL0 Ring 0.</span><span class="sxs-lookup"><span data-stu-id="31100-118">They complete system calls by marshalling them over to the Windows kernel running in VTL0 ring 0.</span></span> <span data-ttu-id="31100-119">VSM crea un pequeño entorno de ejecución que incluye el pequeño kernel seguro que se ejecuta en VTL1 (aislado del kernel y los controladores que se ejecutan en VTL0).</span><span class="sxs-lookup"><span data-stu-id="31100-119">VSM creates a small execution environment that includes the small Secure Kernel executing in VTL1 (isolated from the kernel and drivers running in VTL0).</span></span> <span data-ttu-id="31100-120">La ventaja de seguridad clara es el aislamiento de las páginas del modo de usuario de trustlet de VTL1 de los controladores que se ejecutan en el kernel VTL0.</span><span class="sxs-lookup"><span data-stu-id="31100-120">The clear security benefit is isolation of trustlet user mode pages in VTL1 from drivers running in the VTL0 kernel.</span></span> <span data-ttu-id="31100-121">Aunque el modo kernel de VTL0 esté en peligro por malware, no tendrá acceso a las páginas de proceso de IUM.</span><span class="sxs-lookup"><span data-stu-id="31100-121">Even if kernel mode of VTL0 is compromised by malware, it will not have access to the IUM process pages.</span></span>

<span data-ttu-id="31100-122">Con VSM habilitado, el entorno de la autoridad de seguridad local (LSASS) se ejecuta como trustlet.</span><span class="sxs-lookup"><span data-stu-id="31100-122">With VSM enabled, the Local Security Authority (LSASS) environment runs as a trustlet.</span></span> <span data-ttu-id="31100-123">LSASS administra la Directiva del sistema local, la autenticación de usuarios y la auditoría mientras se manejan los datos de seguridad confidenciales, como los hash de contraseña y las claves de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="31100-123">LSASS manages the local system policy, user authentication, and auditing while handling sensitive security data such as password hashes and Kerberos keys.</span></span> <span data-ttu-id="31100-124">Para aprovechar las ventajas de seguridad de VSM, un trustlet con nombre LSAISO.exe (LSA aislado) se ejecuta en VTL1 y se comunica con LSASS.exe que se ejecutan en VTL0 a través de un canal de RPC.</span><span class="sxs-lookup"><span data-stu-id="31100-124">To leverage the security benefits of VSM, a trustlet named LSAISO.exe (LSA Isolated) runs in VTL1 and communicates with LSASS.exe running in VTL0 through an RPC channel.</span></span> <span data-ttu-id="31100-125">Los secretos de LSAISO se cifran antes de enviarlos a LSASS que se ejecutan en modo de VSM normal y las páginas de LSAISO están protegidas frente a código malintencionado que se ejecuta en VTL0.</span><span class="sxs-lookup"><span data-stu-id="31100-125">The LSAISO secrets are encrypted before sending them over to LSASS running in VSM Normal Mode and the pages of LSAISO are protected from malicious code running in VTL0.</span></span>

<span data-ttu-id="31100-126">**Diagrama 2: diseño de Trustlet de LSASS**</span><span class="sxs-lookup"><span data-stu-id="31100-126">**Diagram 2 – LSASS Trustlet Design**</span></span>

![<span data-ttu-id="31100-127">Diagrama 2: diseño de trustlet de LSASS</span><span class="sxs-lookup"><span data-stu-id="31100-127">diagram 2 – lsass trustlet design</span></span> ](images/lsass-trustlet-design.png)

## <a name="isolated-user-mode-ium-implications"></a><span data-ttu-id="31100-128">Implicaciones del modo de usuario aislado (IUM)</span><span class="sxs-lookup"><span data-stu-id="31100-128">Isolated User Mode (IUM) Implications</span></span>

<span data-ttu-id="31100-129">No es posible asociar a un proceso de IUM, lo que impide la capacidad de depurar el código de VTL1.</span><span class="sxs-lookup"><span data-stu-id="31100-129">It is not possible to attach to an IUM process, inhibiting the ability to debug VTL1 code.</span></span> <span data-ttu-id="31100-130">Esto incluye la depuración posterior a mortem de volcados de memoria y la Asociación de las herramientas de depuración para la depuración en directo.</span><span class="sxs-lookup"><span data-stu-id="31100-130">This includes post mortem debugging of memory dumps and attaching the Debugging Tools for live debugging.</span></span> <span data-ttu-id="31100-131">También incluye los intentos de los controladores de kernel o las cuentas con privilegios para cargar un archivo DLL en un proceso de IUM, para inyectar un subproceso o para proporcionar un APC en modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="31100-131">It also includes attempts by privileged accounts or kernel drivers to load a DLL into an IUM process, to inject a thread, or deliver a user-mode APC.</span></span> <span data-ttu-id="31100-132">Estos intentos pueden dar lugar a la desestabilización de todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="31100-132">Such attempts may result in destabilization of the entire system.</span></span> <span data-ttu-id="31100-133">Las API de Windows que podrían poner en peligro la seguridad de un Trustlet podrían producir errores inesperados.</span><span class="sxs-lookup"><span data-stu-id="31100-133">Windows APIs that would compromise the security of a Trustlet may fail in unexpected ways.</span></span> <span data-ttu-id="31100-134">Por ejemplo, la carga de un archivo DLL en un Trustlet lo hará disponible en VTL0, pero no VTL1.</span><span class="sxs-lookup"><span data-stu-id="31100-134">For example, loading a DLL into a Trustlet will make it available in VTL0 but not VTL1.</span></span> <span data-ttu-id="31100-135">QueueUserApc puede producir un error en modo silencioso si el subproceso de destino está en un Trustlet.</span><span class="sxs-lookup"><span data-stu-id="31100-135">QueueUserApc may silently fail if the target thread is in a Trustlet.</span></span> <span data-ttu-id="31100-136">Otras API, como CreateRemoteThread, VirtualAllocEx y Read/WriteProcessMemory tampoco funcionarán de la manera esperada cuando se usan en Trustlets.</span><span class="sxs-lookup"><span data-stu-id="31100-136">Other APIs, such as CreateRemoteThread, VirtualAllocEx, and Read/WriteProcessMemory will also not work as expected when used against Trustlets.</span></span>

<span data-ttu-id="31100-137">Use el código de ejemplo siguiente para evitar la llamada a cualquier función que intente adjuntar o insertar código en un proceso de IUM.</span><span class="sxs-lookup"><span data-stu-id="31100-137">Use the sample code below to prevent calling any functions which attempt to attach or inject code into an IUM process.</span></span> <span data-ttu-id="31100-138">Esto incluye los controladores de kernel que ponen en cola APC para la ejecución de código en un trustlet.</span><span class="sxs-lookup"><span data-stu-id="31100-138">This includes kernel drivers that queue APCs for execution of code in a trustlet.</span></span>

## <a name="remarks"></a><span data-ttu-id="31100-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="31100-139">Remarks</span></span>

<span data-ttu-id="31100-140">Si el estado de retorno de IsSecureProcess es Success, examine el \_ parámetro out de SecureProcess \_ para determinar si el proceso es un proceso de Ium.</span><span class="sxs-lookup"><span data-stu-id="31100-140">If the return status of IsSecureProcess is success, examine the SecureProcess \_Out\_ parameter to determine if the process is an IUM process.</span></span> <span data-ttu-id="31100-141">Los procesos de IUM están marcados por el sistema para ser "procesos seguros".</span><span class="sxs-lookup"><span data-stu-id="31100-141">IUM processes are marked by the system to be “Secure Processes”.</span></span> <span data-ttu-id="31100-142">Un resultado booleano de TRUE significa que el proceso de destino es de tipo IUM.</span><span class="sxs-lookup"><span data-stu-id="31100-142">A Boolean result of TRUE means the target process is of type IUM.</span></span>


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



<span data-ttu-id="31100-143">WDK para Windows 10, "Windows Driver Kit-Windows 10.0.15063.0", contiene la definición necesaria de la estructura de \_ la \_ información básica extendida del proceso \_ .</span><span class="sxs-lookup"><span data-stu-id="31100-143">The WDK for Windows 10, “Windows Driver Kit - Windows 10.0.15063.0”, contains the required definition of the PROCESS\_EXTENDED\_BASIC\_INFORMATION structure.</span></span> <span data-ttu-id="31100-144">La versión actualizada de la estructura se define en ntddk. h con el nuevo campo IsSecureProcess.</span><span class="sxs-lookup"><span data-stu-id="31100-144">The updated version of the structure is defined in ntddk.h with the new IsSecureProcess field.</span></span>


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



 

 



