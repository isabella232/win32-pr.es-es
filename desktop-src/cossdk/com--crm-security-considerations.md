---
description: Consideraciones de seguridad de COM+ CRM
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Consideraciones de seguridad de COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ababde9f31c0c2655fbf4f0c46b216ca0cbfee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152948"
---
# <a name="com-crm-security-considerations"></a><span data-ttu-id="9347e-103">Consideraciones de seguridad de COM+ CRM</span><span class="sxs-lookup"><span data-stu-id="9347e-103">COM+ CRM Security Considerations</span></span>

<span data-ttu-id="9347e-104">Un archivo de registro de CRM podría contener información confidencial que se debe proteger.</span><span class="sxs-lookup"><span data-stu-id="9347e-104">A CRM log file could contain sensitive information that must be secured.</span></span> <span data-ttu-id="9347e-105">Por este motivo, si la aplicación de servidor se ejecuta con cualquier identidad que no sea el usuario interactivo cuando se crea por primera vez el archivo de registro de CRM, el archivo de registro de CRM está protegido por seguridad para ese usuario.</span><span class="sxs-lookup"><span data-stu-id="9347e-105">For this reason, if the server application is running under any identity other than Interactive User when the CRM log file is first created, the CRM log file is security protected for that user only.</span></span> <span data-ttu-id="9347e-106">Esta característica solo está disponible en el sistema de archivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="9347e-106">This feature is available only on the NTFS file system.</span></span> <span data-ttu-id="9347e-107">Si posteriormente se cambia la identidad de la aplicación de servidor, la información de seguridad del archivo de registro de CRM no se cambia automáticamente.</span><span class="sxs-lookup"><span data-stu-id="9347e-107">If the identity of the server application is subsequently changed, the security information for the CRM log file is not automatically changed.</span></span> <span data-ttu-id="9347e-108">Se puede cambiar manualmente mediante las herramientas de administración de Windows existentes.</span><span class="sxs-lookup"><span data-stu-id="9347e-108">It can be changed manually by using existing Windows administration tools.</span></span> <span data-ttu-id="9347e-109">La alternativa es simplemente eliminar el archivo de registro de CRM cuando está en un estado limpio (lo que se espera después de un cierre controlado de la aplicación de servidor).</span><span class="sxs-lookup"><span data-stu-id="9347e-109">The alternative is simply to delete the CRM log file when it is in a clean state (which is expected after a controlled shutdown of the server application).</span></span>

<span data-ttu-id="9347e-110">En el funcionamiento normal, COM+ crea el componente Compensator de CRM y llama a la interfaz [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) .</span><span class="sxs-lookup"><span data-stu-id="9347e-110">In normal operation, COM+ creates the CRM compensator component and calls the [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) interface.</span></span> <span data-ttu-id="9347e-111">Sin embargo, un usuario con privilegios para crear el compensador de CRM puede llamar a la interfaz **ICrmCompensator** en momentos inadecuados, lo que podría provocar problemas de seguridad del sistema.</span><span class="sxs-lookup"><span data-stu-id="9347e-111">However, a user having privileges to create the CRM Compensator can call the **ICrmCompensator** interface at inappropriate times, possibly causing system security problems.</span></span> <span data-ttu-id="9347e-112">Para ayudar a protegerse frente a estos problemas de seguridad, el administrador del sistema puede usar la seguridad basada en roles para restringir el componente Compensator de CRM solo a las identidades de las aplicaciones de servidor en las que se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="9347e-112">To help protect against these security problems, the system administrator can use role-based security to restrict the CRM Compensator component to only those identities of the server applications in which it runs.</span></span> <span data-ttu-id="9347e-113">Si el componente se ejecuta en una aplicación de biblioteca, esto incluiría todas las identidades de las aplicaciones de servidor.</span><span class="sxs-lookup"><span data-stu-id="9347e-113">If the component is running in a library application, this would include all the identities of the server applications.</span></span>

> [!Note]  
> <span data-ttu-id="9347e-114">A partir de Windows Server 2003, para ayudar a evitar la activación desde fuera de la aplicación de servidor, es posible garantizar un sistema más seguro marcando el componente Compensator de CRM como privado.</span><span class="sxs-lookup"><span data-stu-id="9347e-114">Starting with Windows Server 2003, to help prevent activation from outside the server application, it is possible to further ensure a more secure system by marking the CRM Compensator component as private.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9347e-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9347e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9347e-116">Conceptos de Administrador de recursos de compensación de COM+</span><span class="sxs-lookup"><span data-stu-id="9347e-116">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



