---
title: Modelo de tipo de archivo y asociaciones URI
description: Modelo de tipo de archivo y asociaciones URI
ms.assetid: 4DE7DD08-088A-4E09-B1C7-AE9033EA533D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78540a072405aade01a9f94503999ad105d2078
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078506"
---
# <a name="file-type-and-uri-associations-model"></a><span data-ttu-id="424d5-103">Modelo de tipo de archivo y asociaciones URI</span><span class="sxs-lookup"><span data-stu-id="424d5-103">File type and URI associations model</span></span>

## <a name="platforms"></a><span data-ttu-id="424d5-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="424d5-104">Platforms</span></span>

 <span data-ttu-id="424d5-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="424d5-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="424d5-106">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="424d5-106">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="424d5-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="424d5-107">Description</span></span>

<span data-ttu-id="424d5-108">El tipo de archivo y el modelo de asociación URI han cambiado en Windows 8.</span><span class="sxs-lookup"><span data-stu-id="424d5-108">The file type and URI association model has changed in Windows 8.</span></span> <span data-ttu-id="424d5-109">Las aplicaciones ya no pueden establecerse mediante programación como el controlador predeterminado para un tipo de archivo o URI.</span><span class="sxs-lookup"><span data-stu-id="424d5-109">Apps are no longer able to programmatically set themselves as the default handler for a file type or URI.</span></span> <span data-ttu-id="424d5-110">En su lugar, ahora el usuario controla siempre cuál es el controlador predeterminado para un tipo de archivo o un esquema de URI.</span><span class="sxs-lookup"><span data-stu-id="424d5-110">Instead, now the user always controls what the default handler is for a file type or URI scheme.</span></span>

## <a name="manifestation"></a><span data-ttu-id="424d5-111">Manifestación</span><span class="sxs-lookup"><span data-stu-id="424d5-111">Manifestation</span></span>

<span data-ttu-id="424d5-112">El modo en que se presenta este cambio al usuario depende de cómo esté diseñado la aplicación, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="424d5-112">How this change presents to the user depends upon how the app is designed, for example:</span></span>

-   <span data-ttu-id="424d5-113">Muchas aplicaciones comprueban si son las predeterminadas cada vez que se ejecutan y, si no es así, solicitan al usuario que las establezca como predeterminada.</span><span class="sxs-lookup"><span data-stu-id="424d5-113">Many apps check to see if they are the default every time they run and, if they are not, they prompt the user to set them as default.</span></span> <span data-ttu-id="424d5-114">Sin embargo, dado que las aplicaciones ya no pueden consultar con precisión para determinar qué aplicación es el controlador predeterminado para un tipo de archivo o un esquema de URI, no funciona ninguna de estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="424d5-114">However, because apps can no longer accurately query to determine which app is the default handler for a file type or URI scheme, neither of these operations works.</span></span>
-   <span data-ttu-id="424d5-115">Muchas aplicaciones tienen un cuadro de diálogo o un menú integrado o en su instalador que especifica los tipos de archivo para los que la aplicación debe servir como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="424d5-115">Many apps have a dialog box or menu built in or in their installer that specifies the file types for which the app should serve as the default.</span></span> <span data-ttu-id="424d5-116">Sin embargo, dado que las aplicaciones ya no se pueden establecer mediante programación como el controlador predeterminado para un tipo de archivo o un esquema de URI, esto ya no funciona.</span><span class="sxs-lookup"><span data-stu-id="424d5-116">However, because apps can no longer programmatically set themselves as the default handler for a file type or URI scheme, this no longer works.</span></span>

## <a name="mitigation"></a><span data-ttu-id="424d5-117">Mitigación</span><span class="sxs-lookup"><span data-stu-id="424d5-117">Mitigation</span></span>

<span data-ttu-id="424d5-118">Hay varias cosas que los usuarios pueden hacer para dar cabida a estos cambios:</span><span class="sxs-lookup"><span data-stu-id="424d5-118">There are several things users can do to accommodate these changes:</span></span>

-   <span data-ttu-id="424d5-119">A los usuarios se les pide contextualmente que elijan una aplicación predeterminada para administrar los tipos de archivo, esquemas de URI o ambos cuando no se ha especificado ninguno.</span><span class="sxs-lookup"><span data-stu-id="424d5-119">Users are prompted contextually to choose a default app to handle file types, URI schemes, or both when one has not been specified</span></span>
-   <span data-ttu-id="424d5-120">A los usuarios se les ofrece la opción de cambiar el controlador predeterminado después de instalar nuevas aplicaciones que pueden controlar un tipo de archivo o un esquema de URI.</span><span class="sxs-lookup"><span data-stu-id="424d5-120">Users are offered the option to change their default handler after installing new apps that can handle a file type or URI scheme</span></span>
-   <span data-ttu-id="424d5-121">El panel de control programas predeterminados permite a los usuarios establecer valores predeterminados para una aplicación o un tipo de archivo, un esquema de URI o ambos. las aplicaciones pueden vincularse al panel de control</span><span class="sxs-lookup"><span data-stu-id="424d5-121">The default programs control panel allows users to set defaults for an app, or for a file type, URI scheme, or both; apps can link to the control panel</span></span>
-   <span data-ttu-id="424d5-122">Los valores predeterminados se pueden cambiar desde el explorador de Windows</span><span class="sxs-lookup"><span data-stu-id="424d5-122">Defaults can be changed from Windows Explorer</span></span>

## <a name="solution"></a><span data-ttu-id="424d5-123">Solución</span><span class="sxs-lookup"><span data-stu-id="424d5-123">Solution</span></span>

<span data-ttu-id="424d5-124">Como resultado de estos cambios, se proporciona esta guía de API:</span><span class="sxs-lookup"><span data-stu-id="424d5-124">As a result of these changes, this API guidance is provided:</span></span>

-   <span data-ttu-id="424d5-125">La funcionalidad de algunas llamadas de método dentro de la API de [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) ha cambiado y ya no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="424d5-125">The functionality of some method calls within the [IApplicationAssociationRegistration](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) API has changed, and should no longer be used.</span></span>

    -   <span data-ttu-id="424d5-126">**No** llame a [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault) / [QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) para determinar si una aplicación es la predeterminada.</span><span class="sxs-lookup"><span data-stu-id="424d5-126">**Do not** call [QueryAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefault)/[QueryAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-queryappisdefaultall) to determine if an app is the default</span></span>
    -   <span data-ttu-id="424d5-127">**No** llame a [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) para determinar qué aplicación (si existe) es el valor predeterminado actual.</span><span class="sxs-lookup"><span data-stu-id="424d5-127">**Do not** call [QueryCurrentDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-querycurrentdefault) to determine which app (if any) is the current default</span></span>
    -   <span data-ttu-id="424d5-128">**No** llame a [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault) / [SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) para establecer la aplicación predeterminada</span><span class="sxs-lookup"><span data-stu-id="424d5-128">**Do not** call [SetAppIsDefault](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefault)/[SetAppIsDefaultAll](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationassociationregistration-setappasdefaultall) to set the default app</span></span>

-   <span data-ttu-id="424d5-129">Las instrucciones que se van a avanzar son:</span><span class="sxs-lookup"><span data-stu-id="424d5-129">The guidance going forward is:</span></span>

    -   <span data-ttu-id="424d5-130">**No** consulta para ver qué aplicación es el controlador predeterminado para los tipos de archivos o esquemas de URI</span><span class="sxs-lookup"><span data-stu-id="424d5-130">**Do not** query to see which app is the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="424d5-131">**No** intente supervisar los cambios en el controlador predeterminado para tipos de archivo o esquemas de URI</span><span class="sxs-lookup"><span data-stu-id="424d5-131">**Do not** attempt to monitor changes in the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="424d5-132">**No** intente establecer una aplicación como controlador predeterminado para los tipos de archivos o esquemas de URI.</span><span class="sxs-lookup"><span data-stu-id="424d5-132">**Do not** attempt to set an app as the default handler for file types or URI schemes</span></span>

    -   <span data-ttu-id="424d5-133">**No** intente administrar los valores predeterminados para los tipos de archivos o esquemas de URI desde una aplicación</span><span class="sxs-lookup"><span data-stu-id="424d5-133">**Do not** attempt to manage defaults for file types or URI schemes from within an app</span></span>

    -   <span data-ttu-id="424d5-134">**Realice** la integración con el panel de control [establecer programas predeterminados](../shell/default-programs.md) si quiere permitir que los usuarios de la aplicación ACCEDAn a la interfaz de usuario de administración predeterminada (ya no se admite la interfaz de usuario de administración dentro de la aplicación).</span><span class="sxs-lookup"><span data-stu-id="424d5-134">**Do** integrate with the [Set Default Programs](../shell/default-programs.md) control panel if you want to allow users of your app to access the default management UI (the management UI within the app is no longer supported)</span></span>

        -   <span data-ttu-id="424d5-135">La llamada a [IApplicationAssociationRegistrationUI:: LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) permite al usuario tener acceso a la página del panel de control "[establecer programas predeterminados](../shell/default-programs.md)" de la aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="424d5-135">Calling [IApplicationAssociationRegistrationUI::LaunchAdvancedAssociationUI](/windows/win32/api/shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) allows the user to access the ‘[Set Default Programs](../shell/default-programs.md)’ control panel page for the specified app</span></span>

## <a name="tests"></a><span data-ttu-id="424d5-136">Pruebas</span><span class="sxs-lookup"><span data-stu-id="424d5-136">Tests</span></span>

-   <span data-ttu-id="424d5-137">Prueba para comprobar que las aplicaciones se registran correctamente en el panel de control de establecer programas predeterminados</span><span class="sxs-lookup"><span data-stu-id="424d5-137">Test to verify that apps register properly in Set Default Programs control panel</span></span>
-   <span data-ttu-id="424d5-138">Prueba para comprobar que las aplicaciones se registran correctamente para que aparezcan en la lista OpenWith para los tipos de archivo, esquemas de URI o ambos, que se registran para controlar</span><span class="sxs-lookup"><span data-stu-id="424d5-138">Test to verify that apps register properly to appear in the OpenWith list for the file types, URI schemes, or both, that they register to handle</span></span>
-   <span data-ttu-id="424d5-139">Prueba para comprobar que las nuevas notificaciones de aplicación aparecen después de instalar la aplicación y que el usuario invoca un tipo de archivo, un esquema de URI o ambos, que la aplicación ha registrado para controlar</span><span class="sxs-lookup"><span data-stu-id="424d5-139">Test to verify that new app notifications appear after your app is installed and the user invokes a file type, URI scheme, or both, that your app has registered to handle</span></span>

## <a name="resources"></a><span data-ttu-id="424d5-140">Recursos</span><span class="sxs-lookup"><span data-stu-id="424d5-140">Resources</span></span>

-   <span data-ttu-id="424d5-141">[Prácticas recomendadas para las asociaciones de tipo de archivo y URI en aplicaciones de escritorio de Windows 8](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="424d5-141">[Best Practices for File Type and URI Associations in Windows 8 Desktop Apps](/previous-versions/windows/desktop/legacy/cc144156(v=vs.85))</span></span>
-   [<span data-ttu-id="424d5-142">Presentación de las asociaciones de tipo de archivo y de generación automática</span><span class="sxs-lookup"><span data-stu-id="424d5-142">File Type Associations and AutoPlay Build Conference Presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/PLAT-282T)

 

 