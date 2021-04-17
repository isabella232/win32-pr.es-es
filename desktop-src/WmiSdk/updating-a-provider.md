---
description: En ocasiones, es posible que necesite instalar una versión más reciente de un proveedor en un sistema en ejecución.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Actualizar un proveedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697414"
---
# <a name="updating-a-provider"></a><span data-ttu-id="680a4-103">Actualizar un proveedor</span><span class="sxs-lookup"><span data-stu-id="680a4-103">Updating a Provider</span></span>

<span data-ttu-id="680a4-104">En ocasiones, es posible que necesite instalar una versión más reciente de un proveedor en un sistema en ejecución.</span><span class="sxs-lookup"><span data-stu-id="680a4-104">Sometimes you may need to install a newer version of a provider onto a running system.</span></span> <span data-ttu-id="680a4-105">Si el proveedor está instalado como un archivo DLL, puede instalar un nuevo proveedor sin tener que reiniciar el servicio, reiniciar el equipo o afectar de algún modo a las aplicaciones que usan WMI en ese momento.</span><span class="sxs-lookup"><span data-stu-id="680a4-105">If your provider is installed as a DLL, you can install a new provider without having to restart the service, reboot the computer, or otherwise affect any applications using WMI at that time.</span></span>

<span data-ttu-id="680a4-106">En el procedimiento siguiente se describe cómo actualizar un proveedor.</span><span class="sxs-lookup"><span data-stu-id="680a4-106">The following procedure describes how to update a provider.</span></span>

<span data-ttu-id="680a4-107">**Para actualizar un proveedor**</span><span class="sxs-lookup"><span data-stu-id="680a4-107">**To update a provider**</span></span>

1.  <span data-ttu-id="680a4-108">Cree el nuevo proveedor.</span><span class="sxs-lookup"><span data-stu-id="680a4-108">Build the new provider.</span></span>

    1.  <span data-ttu-id="680a4-109">Compile el nuevo proveedor con un nombre de archivo DLL diferente y un **CLSID** diferente.</span><span class="sxs-lookup"><span data-stu-id="680a4-109">Compile the new provider with a different DLL name and a different **CLSID**.</span></span>

        <span data-ttu-id="680a4-110">Por ejemplo, cambie Myprov.dll a Myprov1.dll y **CLSID \_ MyProProv** a **CLSID \_ MyProv** 1.</span><span class="sxs-lookup"><span data-stu-id="680a4-110">For example, change Myprov.dll to Myprov1.dll, and **CLSID\_MyProProv** to **CLSID\_MyProv** 1.</span></span>

    2.  <span data-ttu-id="680a4-111">Modifique el archivo MOF de registro del proveedor para usar el nuevo CLSID (CLSID \_ MyProv1), pero el mismo nombre de proveedor ("MyProv").</span><span class="sxs-lookup"><span data-stu-id="680a4-111">Modify the provider registration MOF file to use the new CLSID (CLSID\_MyProv1), but the same provider name ("MyProv").</span></span>

2.  <span data-ttu-id="680a4-112">Instale el nuevo proveedor.</span><span class="sxs-lookup"><span data-stu-id="680a4-112">Install the new provider.</span></span>

    1.  <span data-ttu-id="680a4-113">Copie el nuevo archivo DLL de proveedor con el nuevo nombre junto con el anterior.</span><span class="sxs-lookup"><span data-stu-id="680a4-113">Copy the new provider DLL with the new name alongside the old one.</span></span>
    2.  <span data-ttu-id="680a4-114">Registre automáticamente el nuevo proveedor.</span><span class="sxs-lookup"><span data-stu-id="680a4-114">Self-register the new provider.</span></span>

        <span data-ttu-id="680a4-115">Por ejemplo, use el comando **regsvr32** **myprov1.dll** para registrar el nuevo proveedor.</span><span class="sxs-lookup"><span data-stu-id="680a4-115">For example, use the **regsvr32** **myprov1.dll** command to register the new provider.</span></span>

    3.  <span data-ttu-id="680a4-116">Compile el nuevo registro del proveedor MOF, con lo que se sobrescribirá el registro del proveedor anterior.</span><span class="sxs-lookup"><span data-stu-id="680a4-116">Compile the new provider registration MOF, thus overwriting the old provider registration.</span></span> <span data-ttu-id="680a4-117">Hasta este punto, el proveedor anterior era totalmente funcional. ahora el nuevo proveedor está totalmente operativo.</span><span class="sxs-lookup"><span data-stu-id="680a4-117">Until this point, the old provider was fully functional; now the new provider is fully operational.</span></span>

3.  <span data-ttu-id="680a4-118">Quite la versión anterior del proveedor, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="680a4-118">Remove the old version of the provider, if necessary.</span></span>

    1.  <span data-ttu-id="680a4-119">Anule el registro del archivo DLL antiguo.</span><span class="sxs-lookup"><span data-stu-id="680a4-119">Unregister the old DLL.</span></span>

        <span data-ttu-id="680a4-120">Por ejemplo, use el comando **regsvr32** **/umyprov.dll** para anular el registro del archivo dll antiguo.</span><span class="sxs-lookup"><span data-stu-id="680a4-120">For example, use the **regsvr32** **/umyprov.dll** command to unregister the old DLL.</span></span>

    2.  <span data-ttu-id="680a4-121">Marque el archivo DLL anterior que se eliminará al reiniciar llamando a [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).</span><span class="sxs-lookup"><span data-stu-id="680a4-121">Mark the old DLL to be deleted on reboot by calling [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).</span></span>

<span data-ttu-id="680a4-122">Puede realizar pasos similares para actualizar un proveedor implementado en el servidor local.</span><span class="sxs-lookup"><span data-stu-id="680a4-122">You can take similar steps to upgrade a local server-implemented provider.</span></span>

## <a name="related-topics"></a><span data-ttu-id="680a4-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="680a4-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="680a4-124">Desarrollar un proveedor WMI</span><span class="sxs-lookup"><span data-stu-id="680a4-124">Developing a WMI Provider</span></span>](developing-a-wmi-provider.md)
</dt> <dt>

[<span data-ttu-id="680a4-125">Configuración de descriptores de seguridad de espacio</span><span class="sxs-lookup"><span data-stu-id="680a4-125">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="680a4-126">Protección del proveedor</span><span class="sxs-lookup"><span data-stu-id="680a4-126">Securing Your Provider</span></span>](securing-your-provider.md)
</dt> </dl>

 

 
