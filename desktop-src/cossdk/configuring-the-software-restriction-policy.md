---
description: Configuración de la Directiva de restricción de software
ms.assetid: 22c1897a-abb5-4ce9-9d09-21b6aed4f1d8
title: Configuración de la Directiva de restricción de software
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 522f216af6957ebd23bc9f17c70f61cab2cabc5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080269"
---
# <a name="configuring-the-software-restriction-policy"></a><span data-ttu-id="fe5cc-103">Configuración de la Directiva de restricción de software</span><span class="sxs-lookup"><span data-stu-id="fe5cc-103">Configuring the Software Restriction Policy</span></span>

<span data-ttu-id="fe5cc-104">Cuando se establecen explícitamente los niveles de confianza de la Directiva de restricción de software de una aplicación COM+, se invalida la configuración predeterminada de todo el sistema.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-104">When you explicitly set the software restriction policy trust levels of a COM+ application, you are overriding the default systemwide settings.</span></span> <span data-ttu-id="fe5cc-105">Esto suele ser necesario para las aplicaciones de servidor COM+, ya que el nivel de confianza de todo el sistema se establece en todas las aplicaciones de servidor (ya que todos se ejecutan en el mismo archivo, dllhost.exe).</span><span class="sxs-lookup"><span data-stu-id="fe5cc-105">This is often necessary for COM+ server applications because the systemwide trust level is set the same for all server applications (because they all run in the same file, dllhost.exe).</span></span> <span data-ttu-id="fe5cc-106">Sin embargo, al establecer el nivel de confianza de la Directiva de restricción de software de una aplicación de biblioteca COM+, afecta a la configuración de todo el sistema para esa aplicación.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-106">However, when you set the software restriction policy trust level of a COM+ library application, you are affecting the systemwide configuration for that application.</span></span> <span data-ttu-id="fe5cc-107">Para obtener una explicación de cómo usar la Directiva de restricción de software en COM+, consulte [usar la Directiva de restricción de software en com+](using-the-software-restriction-policy-in-com-.md).</span><span class="sxs-lookup"><span data-stu-id="fe5cc-107">For a discussion of how to use the software restriction policy in COM+, see [Using the Software Restriction Policy in COM+](using-the-software-restriction-policy-in-com-.md).</span></span>

<span data-ttu-id="fe5cc-108">**Para establecer la Directiva de restricción de software**</span><span class="sxs-lookup"><span data-stu-id="fe5cc-108">**To set the software restriction policy**</span></span>

1.  <span data-ttu-id="fe5cc-109">Haga clic con el botón secundario en la aplicación COM+ para la que está configurando la Directiva de restricción de software y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-109">Right-click the COM+ application for which you are setting the software restriction policy, and then click **Properties**.</span></span>

2.  <span data-ttu-id="fe5cc-110">En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .</span><span class="sxs-lookup"><span data-stu-id="fe5cc-110">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="fe5cc-111">En **Directiva de restricción de software**, active la casilla **aplicar Directiva de restricción de software** ; Esto le permite establecer el nivel de confianza.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-111">Under **Software Restriction Policy**, select the **Apply software restriction policy** check box; this enables you to set the trust level.</span></span> <span data-ttu-id="fe5cc-112">Si desactiva la casilla, COM+ usará la configuración de todo el sistema de la Directiva de restricción de software para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-112">Clearing the check box will cause COM+ to use the systemwide configuration of the software restriction policy for the application.</span></span> <span data-ttu-id="fe5cc-113">Esta casilla corresponde a la propiedad SRPEnabled de la colección de [**aplicaciones**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5cc-113">This check box corresponds to the SRPEnabled property of the [**Applications**](applications.md) collection.</span></span>

4.  <span data-ttu-id="fe5cc-114">En el cuadro **nivel de restricción** , seleccione el nivel adecuado.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-114">In the **Restriction Level** box, select the appropriate level.</span></span> <span data-ttu-id="fe5cc-115">Este cuadro desplegable corresponde a la propiedad SRPTrustLevel de la colección de [**aplicaciones**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="fe5cc-115">This drop-down box corresponds to the SRPTrustLevel property of the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="fe5cc-116">Los niveles son los siguientes, ordenados de menor a mayor confianza:</span><span class="sxs-lookup"><span data-stu-id="fe5cc-116">The levels are as follows, ordered from least to most trusted:</span></span>

    -   <span data-ttu-id="fe5cc-117">No **permitido**.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-117">**Disallowed**.</span></span> <span data-ttu-id="fe5cc-118">No se permite que la aplicación use los privilegios completos del usuario.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-118">The application is disallowed from using the full privileges of the user.</span></span> <span data-ttu-id="fe5cc-119">Los componentes con cualquier nivel de confianza pueden cargarse en él.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-119">Components with any trust level can be loaded into it.</span></span>
    -   <span data-ttu-id="fe5cc-120">**Sin restricciones**.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-120">**Unrestricted**.</span></span> <span data-ttu-id="fe5cc-121">La aplicación tiene acceso ilimitado a los privilegios del usuario.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-121">The application has unrestricted access to the user's privileges.</span></span> <span data-ttu-id="fe5cc-122">Solo se pueden cargar en él los componentes con un nivel de confianza no restringido.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-122">Only components with an Unrestricted trust level can be loaded into it.</span></span>

5.  <span data-ttu-id="fe5cc-123">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="fe5cc-123">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fe5cc-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fe5cc-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe5cc-125">Configuración de la seguridad de Role-Based</span><span class="sxs-lookup"><span data-stu-id="fe5cc-125">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="fe5cc-126">Habilitar la autenticación para una aplicación de biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe5cc-126">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="fe5cc-127">Establecer un nivel de autenticación para una aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="fe5cc-127">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> <dt>

[<span data-ttu-id="fe5cc-128">Establecer un nivel de suplantación</span><span class="sxs-lookup"><span data-stu-id="fe5cc-128">Setting an Impersonation Level</span></span>](setting-an-impersonation-level.md)
</dt> </dl>

 

 



