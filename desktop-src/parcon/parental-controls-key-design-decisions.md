---
description: Decisiones de diseño clave de controles parentales
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Decisiones de diseño clave de controles parentales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39cb4be775a3380cb9fe7aa677362df31a2dc453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083366"
---
# <a name="parental-controls-key-design-decisions"></a><span data-ttu-id="77ad6-103">Decisiones de diseño clave de controles parentales</span><span class="sxs-lookup"><span data-stu-id="77ad6-103">Parental Controls Key Design Decisions</span></span>

<span data-ttu-id="77ad6-104">Las decisiones de diseño principales en el desarrollo de controles parentales de Windows Vista son:</span><span class="sxs-lookup"><span data-stu-id="77ad6-104">Major design decisions in the development of Windows Vista Parental Controls are:</span></span>

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a><span data-ttu-id="77ad6-105">Dependencia esencial de la característica control de cuentas de usuario (UAC) de Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77ad6-105">Essential Dependency on Windows Vista User Account Control (UAC) Feature</span></span>

<span data-ttu-id="77ad6-106">Una decisión clave de los controles parentales de Windows Vista es basarse en la nueva característica control de cuentas de usuario (UAC) para implementar las identidades de cuenta de derechos reducidas que se necesitan especialmente para las restricciones sin conexión en los usuarios controlados.</span><span class="sxs-lookup"><span data-stu-id="77ad6-106">A key decision for Windows Vista Parental Controls is to rely on the new User Account Control (UAC) feature to implement the reduced rights account identities especially needed for offline restrictions on controlled users.</span></span> <span data-ttu-id="77ad6-107">Para obtener más información acerca de UAC, vea [la historia de desarrollador de Windows Vista y Windows Server 2008: requisitos de desarrollo de aplicaciones de Windows Vista para el control de cuentas de usuario (UAC)](/previous-versions/aa905330(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="77ad6-107">For more information about UAC, see [The Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10)).</span></span> <span data-ttu-id="77ad6-108">En Resumen, cada cuenta con derechos de administrador tiene privilegios para llevar a cabo el rol primario o tutor para ver los datos de registro y establecer directivas.</span><span class="sxs-lookup"><span data-stu-id="77ad6-108">In summary, every account with administrator rights effectively has privileges to perform the parent or guardian role of viewing log data and setting policies.</span></span> <span data-ttu-id="77ad6-109">Los controles parentales solo se pueden establecer en los usuarios de derechos estándar (anteriormente denominados cuentas de usuario con privilegios mínimos o LUAs), ya que solo pueden modificar los registros y los valores de configuración con Access Control listas (ACL) configuradas únicamente para que los administradores escriban.</span><span class="sxs-lookup"><span data-stu-id="77ad6-109">Parental controls may only be set on standard-rights users (formerly called Least-privileged User Accounts, or LUAs), as only they cannot alter logs and settings with Access Control Lists (ACLs) configured only for administrators to write.</span></span> <span data-ttu-id="77ad6-110">En otras palabras:</span><span class="sxs-lookup"><span data-stu-id="77ad6-110">In other words:</span></span>

-   <span data-ttu-id="77ad6-111">Una identidad primaria o de protección es igual de forma implícita a una cuenta que tenga derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="77ad6-111">A parent or guardian identity implicitly equals an account that has rights of an administrator.</span></span>
-   <span data-ttu-id="77ad6-112">Los usuarios bajo control parental deben ser usuarios estándar.</span><span class="sxs-lookup"><span data-stu-id="77ad6-112">Parentally controlled users must be standard users.</span></span>

## <a name="nearly-all-settings-are-available-by-apis"></a><span data-ttu-id="77ad6-113">Casi todas las configuraciones están disponibles en las API</span><span class="sxs-lookup"><span data-stu-id="77ad6-113">Nearly All Settings Are Available by APIs</span></span>

<span data-ttu-id="77ad6-114">Con la excepción de los elementos como las definiciones del sistema de clasificación, las API expuestas también pueden modificar la configuración disponible para su manipulación por parte de la interfaz de usuario de controles parentales.</span><span class="sxs-lookup"><span data-stu-id="77ad6-114">With the exception of items such as ratings system definitions, settings available for manipulation by the Parental Controls User Interface may also be modified by exposed APIs.</span></span> <span data-ttu-id="77ad6-115">Es necesario que los programas implementen la elevación de derechos administrativos para modificar la configuración, como se indicó anteriormente para UAC.</span><span class="sxs-lookup"><span data-stu-id="77ad6-115">It is necessary for programs to implement elevation to administrative rights in order to alter settings, as noted above for UAC.</span></span>

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a><span data-ttu-id="77ad6-116">El control parental de Windows Vista es una tecnología solo para consumidores</span><span class="sxs-lookup"><span data-stu-id="77ad6-116">Windows Vista Parental Controls Is a Consumer-only Technology</span></span>

<span data-ttu-id="77ad6-117">Los controles parentales de Windows Vista no están diseñados para usarse con cuentas de dominio.</span><span class="sxs-lookup"><span data-stu-id="77ad6-117">Windows Vista Parental Controls are not intended to be used with domain accounts.</span></span> <span data-ttu-id="77ad6-118">Como tecnología de consumidor, el control parental no se implementa en las SKU comerciales de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="77ad6-118">As a consumer technology, Parental Controls is not deployed in business SKUs of Windows Vista.</span></span> <span data-ttu-id="77ad6-119">Si un equipo está unido a un dominio, se suprimirán los vínculos de la interfaz de usuario de seguridad de la familia.</span><span class="sxs-lookup"><span data-stu-id="77ad6-119">If a computer is joined to a domain, the Family Safety user interface links will be suppressed.</span></span>

<span data-ttu-id="77ad6-120">Se proporcionará un mecanismo para exponer la funcionalidad del caso unido al dominio, pero solo se pueden configurar cuentas de usuario que no sean de dominio con controles parentales.</span><span class="sxs-lookup"><span data-stu-id="77ad6-120">A mechanism will be provided to expose the functionality for the domain-joined case, but only non-domain user accounts may be configured with Parental Controls.</span></span>

 

 
