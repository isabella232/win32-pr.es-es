---
description: El controlador de filtro debe estar registrado. También puede buscar un controlador de filtro existente para una extensión de nombre de archivo determinada a través del registro o mediante la interfaz ILoadFilter.
ms.assetid: 3478b948-73c7-4533-974a-d9b5186a651b
title: Registrar controladores de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f39688bbea3bb0dd73ef28a0ba6e8b0dcf7977
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153970"
---
# <a name="registering-filter-handlers"></a><span data-ttu-id="a7cf1-104">Registrar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="a7cf1-104">Registering Filter Handlers</span></span>

<span data-ttu-id="a7cf1-105">El controlador de filtro debe estar registrado.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-105">Your filter handler must be registered.</span></span> <span data-ttu-id="a7cf1-106">También puede buscar un controlador de filtro existente para una extensión de nombre de archivo determinada a través del registro o mediante la interfaz [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) .</span><span class="sxs-lookup"><span data-stu-id="a7cf1-106">You can also locate an existing filter handler for a given file name extension either through the registry or by using the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface.</span></span>

<span data-ttu-id="a7cf1-107">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a7cf1-107">This topic is organized as follows:</span></span>

- [<span data-ttu-id="a7cf1-108">Registro de controladores de filtros para Windows Search</span><span class="sxs-lookup"><span data-stu-id="a7cf1-108">Registering Filters Handlers for Windows Search</span></span>](#registering-filter-handlers)
  - [<span data-ttu-id="a7cf1-109">Enfoque obsoleto para registrar controladores de filtros</span><span class="sxs-lookup"><span data-stu-id="a7cf1-109">Obsolete Approach for Registering Filters Handlers</span></span>](#obsolete-approach-for-registering-filters-handlers)
- [<span data-ttu-id="a7cf1-110">Reemplazar controladores de filtro existentes</span><span class="sxs-lookup"><span data-stu-id="a7cf1-110">Replacing Existing Filter Handlers</span></span>](#replacing-existing-filter-handlers)
- [<span data-ttu-id="a7cf1-111">Buscar un controlador de filtro para una extensión de archivo determinada</span><span class="sxs-lookup"><span data-stu-id="a7cf1-111">Finding a Filter Handler for a Given File Extension</span></span>](#finding-a-filter-handler-for-a-given-file-extension)
- [<span data-ttu-id="a7cf1-112">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a7cf1-112">Additional Resources</span></span>](#additional-resources)
- [<span data-ttu-id="a7cf1-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a7cf1-113">Related topics</span></span>](#related-topics)

> [!NOTE]  
> <span data-ttu-id="a7cf1-114">Un controlador de filtro es una implementación de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="a7cf1-114">A filter handler is an implementation of the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

## <a name="registering-filters-handlers-for-windows-search"></a><span data-ttu-id="a7cf1-115">Registro de controladores de filtros para Windows Search</span><span class="sxs-lookup"><span data-stu-id="a7cf1-115">Registering Filters Handlers for Windows Search</span></span>

<span data-ttu-id="a7cf1-116">En la tabla siguiente se enumeran los GUID necesarios para registrar un nuevo controlador de protocolo o para buscar un controlador de protocolo existente.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-116">The GUIDs you need for registering a new protocol handler or to find an existing protocol handler are listed in the following table.</span></span>

| <span data-ttu-id="a7cf1-117">GUID</span><span class="sxs-lookup"><span data-stu-id="a7cf1-117">GUID</span></span>                                     | <span data-ttu-id="a7cf1-118">Definido por el usuario o la aplicación</span><span class="sxs-lookup"><span data-stu-id="a7cf1-118">User or application defined</span></span> | <span data-ttu-id="a7cf1-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7cf1-119">Description</span></span>                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7cf1-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span><span class="sxs-lookup"><span data-stu-id="a7cf1-120">**89BCB740-6119-101A-BCB7-00DD010655AF**</span></span> | <span data-ttu-id="a7cf1-121">Application</span><span class="sxs-lookup"><span data-stu-id="a7cf1-121">Application</span></span>                 | <span data-ttu-id="a7cf1-122">El GUID de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) es una constante de clave del registro para todos los controladores de filtro.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-122">The [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface GUID is a registry key constant for all filter handlers.</span></span> |
| <span data-ttu-id="a7cf1-123">**{PersistentHandlerGUID}**</span><span class="sxs-lookup"><span data-stu-id="a7cf1-123">**{PersistentHandlerGUID}**</span></span>              | <span data-ttu-id="a7cf1-124">User (Usuario)</span><span class="sxs-lookup"><span data-stu-id="a7cf1-124">User</span></span>                        | <span data-ttu-id="a7cf1-125">Este es el GUID del controlador persistente.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-125">This is the GUID for the persistent handler.</span></span>                                                              |
| <span data-ttu-id="a7cf1-126">**{FilterHandlerCLSID}**</span><span class="sxs-lookup"><span data-stu-id="a7cf1-126">**{FilterHandlerCLSID}**</span></span>                 | <span data-ttu-id="a7cf1-127">User (Usuario)</span><span class="sxs-lookup"><span data-stu-id="a7cf1-127">User</span></span>                        | <span data-ttu-id="a7cf1-128">Este es el identificador de clase (CLSID) para el controlador de filtro.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-128">This is the class identifier (CLSID) for the filter handler.</span></span>                                              |
| <span data-ttu-id="a7cf1-129">**{ApplicationGUID}**</span><span class="sxs-lookup"><span data-stu-id="a7cf1-129">**{ApplicationGUID}**</span></span>                    | <span data-ttu-id="a7cf1-130">User (Usuario)</span><span class="sxs-lookup"><span data-stu-id="a7cf1-130">User</span></span>                        | <span data-ttu-id="a7cf1-131">Se trata de un GUID intermedio (agregado).</span><span class="sxs-lookup"><span data-stu-id="a7cf1-131">This is an intermediate (aggregated) GUID.</span></span>                                                                |

<span data-ttu-id="a7cf1-132">Los controladores de filtro deben estar registrados en \_ \_ el equipo local hkey porque SearchFilterHost.exe se está ejecutando en la cuenta del sistema y, por tanto, no pueden tener acceso a las claves del registro para \_ el usuario actual de HKEY \_ para el usuario que ha iniciado sesión.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-132">Filter handlers must be registered in HKEY\_LOCAL\_MACHINE because SearchFilterHost.exe is running under the SYSTEM account and therefore cannot access registry keys for HKEY\_CURRENT\_USER for the logged-on user.</span></span> <span data-ttu-id="a7cf1-133">Además, el grupo de usuarios debe tener acceso de lectura y ejecución al controlador de filtro. dll porque SearchFilterHost.exe quita todos los derechos de administrador y solo permite derechos que no son de administrador.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-133">In addition, the Users group must have read-and-execute access to the filter handler .dll itself because SearchFilterHost.exe removes all administrator rights and permits only non-administrator rights.</span></span> <span data-ttu-id="a7cf1-134">Dado que la ubicación predeterminada del proyecto de Visual Studio se encuentra en el directorio del usuario actual y, por tanto, no concede permisos de lectura al grupo de usuarios, debe trasladar el archivo. dll o cambiar las ACL para permitir el acceso a SearchFilterHost.exe.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-134">Because the default Visual Studio project location is in the current user's directory, and so does not give read permissions to the Users group, you must either move the .dll or change the ACLs to allow SearchFilterHost.exe access.</span></span>

<span data-ttu-id="a7cf1-135">Al registrar un nuevo controlador de filtro, se recomienda usar un nombre descriptivo, por ejemplo, HTML IFilter.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-135">When you register a new filter handler, we recommend that you use a descriptive name, for example, HTML IFilter.</span></span>

<span data-ttu-id="a7cf1-136">**Para registrar el nuevo controlador de filtro:**</span><span class="sxs-lookup"><span data-stu-id="a7cf1-136">**To register your new filter handler:**</span></span>

1. <span data-ttu-id="a7cf1-137">Especifique la extensión y el GUID del controlador persistente que usará el controlador de filtro:</span><span class="sxs-lookup"><span data-stu-id="a7cf1-137">Specify the extension and persistent handler GUID that will use the filter handler:</span></span>

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                PersistentHandler
                   (Default) = {PersistentHandlerGUID}
```

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {PersistentHandlerGUID}
                      PersistentAddinsRegistered
                         {89BCB740-6119-101A-BCB7-00DD010655AF}l
                            (Default) = {FilterHandlerCLSID}
```

2. <span data-ttu-id="a7cf1-138">Registre el controlador de filtro con las claves y los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="a7cf1-138">Register your filter handler with the following keys and values:</span></span>

```
    HKEY_LOCAL_MACHINE
       Software
          Classes
             .txt
                CLSID
                   {FilterHandlerCLSID}
                      (Default) = {DescriptiveFilterHandlerName}
                      InprocServer32
                         (Default) = DLL Install Path
                         ThreadingModel = Both
```

### <a name="obsolete-approach-for-registering-filters-handlers"></a><span data-ttu-id="a7cf1-139">Enfoque obsoleto para registrar controladores de filtros</span><span class="sxs-lookup"><span data-stu-id="a7cf1-139">Obsolete Approach for Registering Filters Handlers</span></span>

<span data-ttu-id="a7cf1-140">Este enfoque no se recomienda para su uso.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-140">This approach is not recommended for use.</span></span> <span data-ttu-id="a7cf1-141">Los filtros se pueden registrar para un CLSID que representa una clase de modelo de objetos componentes (COM) y/o para una extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-141">Filters can be registered for a CLSID that represents a Component Object Model (COM) class, and/or for a file name extension.</span></span> <span data-ttu-id="a7cf1-142">Podría registrar ambos filtros si necesita registrar un controlador de filtro para una clase y un controlador de filtro diferente para una extensión de nombre de archivo dentro de la clase.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-142">You could register both filters if you need to register a filter handler for a class, and a different filter handler for a file name extension within the class.</span></span> <span data-ttu-id="a7cf1-143">Tenga en cuenta que un controlador de filtro registrado para una extensión de nombre de archivo tiene prioridad sobre un controlador de filtro para un CLSID.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-143">Note that a filter handler registered for a file name extension takes precedence over a filter handler for a CLSID.</span></span>

<span data-ttu-id="a7cf1-144">Estas entradas son entradas del registro OLE estándar hasta la entrada de la clase **CLSID \\ {ApplicationGUID}**, inclusive.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-144">These entries are standard OLE registry entries up to and including the entry for the class **CLSID\\{ApplicationGUID}**.</span></span> <span data-ttu-id="a7cf1-145">El sample.dll DLL implementa el comportamiento del objeto en ejecución para la clase. txt.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-145">The DLL sample.dll implements running object behavior for the .txt class.</span></span> <span data-ttu-id="a7cf1-146">Observe la entrada adicional, PersistentHandler.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-146">Note the extra entry, PersistentHandler.</span></span> <span data-ttu-id="a7cf1-147">Esta entrada especifica la clase responsable de las solicitudes de agente a los objetos persistentes de la clase de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-147">This entry specifies the class that is responsible for brokering requests to the persistent objects of the sample class.</span></span> <span data-ttu-id="a7cf1-148">La entrada en **PersistentAddinsRegistered** identifica la implementación responsable de la interfaz denominada **89BCB740-6119-101A-BCB7-00DD010655AF**(IID \_ IFilter).</span><span class="sxs-lookup"><span data-stu-id="a7cf1-148">The entry under **PersistentAddinsRegistered** identifies the implementation responsible for the interface named **89BCB740-6119-101A-BCB7-00DD010655AF**(IID\_IFilter).</span></span> <span data-ttu-id="a7cf1-149">La clase que implementa el **\_ IFilter de IID** tiene entradas de registro estándar de OLE.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-149">The class implementing **IID\_IFilter** has standard OLE registry entries.</span></span> <span data-ttu-id="a7cf1-150">La DLL InprocServer32 se carga a través del mecanismo estándar de OLE.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-150">The InprocServer32 DLL is loaded through the standard OLE mechanism.</span></span>

<span data-ttu-id="a7cf1-151">Windows Search observa el modelo de subprocesos especificado para el controlador de filtro.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-151">Windows Search observes the threading model specified for the filter handler.</span></span> <span data-ttu-id="a7cf1-152">Cuando el modelo de subprocesos se establece en **ambos**, el controlador de filtro debe ser seguro para subprocesos; de lo contrario, si no es seguro para subprocesos, especifique **Apartment**.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-152">When the threading model is set to **Both**, the filter handler must be thread safe; otherwise, if it is not thread safe, specify **Apartment**.</span></span> <span data-ttu-id="a7cf1-153">Tenga en cuenta que los controladores de filtro siempre deben ser seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-153">Note that filter handlers should always be thread safe.</span></span>

<span data-ttu-id="a7cf1-154">Las siguientes entradas del registro de ejemplo son para un controlador de filtro registrado para una extensión de nombre de archivo y una clase.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-154">The following example registry entries are for a filter handler registered for a class and file name extension.</span></span> <span data-ttu-id="a7cf1-155">**{PersistentHandlerGUID}** y **{FilterHandlerCLSID}** se usan como variables que indican valores que deben ser especificados por el creador del controlador de filtro.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-155">**{PersistentHandlerGUID}** and **{FilterHandlerCLSID}** are used as variables indicating values that need to be specified by the creator of the filter handler.</span></span> <span data-ttu-id="a7cf1-156">Los valores son de tipo REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-156">The values are of type REG\_SZ.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Classes
         .txt
            (Default) = SampleFile
         SampleFile
            (Default) = Class for Sample Files
            CLSID
               (Default) = {ApplicationGUID}
         CLSID
            {ApplicationGUID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sample.dll
               PersistentHandler
                  (Default) = {PersistentHandlerGUID}
            {PersistentHandlerGUID}
               (Default) = Sample file persistent handler
               PersistentAddinsRegistered
                  {89BCB740-6119-101A-BCB7-00DD010655AF}l
                     (Default) = {FilterHandlerCLSID}
            {FilterHandlerCLSID}
               (Default) = Sample Files
               InprocServer32
                  (Default) = sampfilt.dll
                  ThreadingModel = Both
```

## <a name="replacing-existing-filter-handlers"></a><span data-ttu-id="a7cf1-157">Reemplazar controladores de filtro existentes</span><span class="sxs-lookup"><span data-stu-id="a7cf1-157">Replacing Existing Filter Handlers</span></span>

<span data-ttu-id="a7cf1-158">Se recomienda no reemplazar los controladores de filtro integrados para los tipos de archivo comunes, como. txt,. doc,. html,. URL, etc., ya que esto puede tener efectos no deseados en otros componentes del sistema.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-158">We recommend that you do not replace the built-in filter handlers for common file types such as .txt, .doc, .html, .url, and so forth, because doing so can have undesired effects on other system components.</span></span> <span data-ttu-id="a7cf1-159">La indexación de cuerpos de mensaje de correo electrónico depende de los controladores de filtro. txt,. html y. rtf, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-159">Indexing email message bodies depends on the .txt, .html, and .rtf filter handlers, for example.</span></span>

<span data-ttu-id="a7cf1-160">Si se va a instalar un nuevo controlador de filtro para un tipo de archivo como sustituto de un registro de filtro existente, el instalador debe guardar el registro actual y restaurarlo si se desinstala el nuevo controlador de filtro.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-160">If a new filter handler for a file type is being installed as a replacement for an existing filter registration, the installer should save the current registration and restore it if the new filter handler is uninstalled.</span></span> <span data-ttu-id="a7cf1-161">No hay ningún mecanismo para encadenar filtros.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-161">There is no mechanism to chain filters.</span></span> <span data-ttu-id="a7cf1-162">Por lo tanto, el nuevo controlador de filtro es responsable de replicar cualquier funcionalidad necesaria del filtro antiguo.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-162">Hence, the new filter handler is responsible for replicating any necessary functionality of the old filter.</span></span>

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a><span data-ttu-id="a7cf1-163">Buscar un controlador de filtro para una extensión de archivo determinada</span><span class="sxs-lookup"><span data-stu-id="a7cf1-163">Finding a Filter Handler for a Given File Extension</span></span>

<span data-ttu-id="a7cf1-164">Puede usar la interfaz [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) para buscar un controlador de filtro para una extensión de nombre de archivo determinada.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-164">You can use the [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) interface to find a filter handler for a given file name extension.</span></span> <span data-ttu-id="a7cf1-165">En las entradas del registro de ejemplo siguiente se muestra cómo hacerlo para los archivos HTML.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-165">The following example registry entries illustrate how to do so for HTML files.</span></span> <span data-ttu-id="a7cf1-166">En este ejemplo, el controlador de filtro para documentos HTML es nlhtml.dll.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-166">In this example, the filter handler for HTML documents is nlhtml.dll.</span></span> <span data-ttu-id="a7cf1-167">Los valores son de tipo REG \_ SZ.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-167">The values are of type REG\_SZ.</span></span>

<span data-ttu-id="a7cf1-168">**Para buscar el controlador de filtro para una extensión de nombre de archivo determinada:**</span><span class="sxs-lookup"><span data-stu-id="a7cf1-168">**To find the filter handler for a given file name extension:**</span></span>

1. <span data-ttu-id="a7cf1-169">Compruebe si la extensión del tipo de archivos filtrados tiene un controlador persistente registrado en la entrada del registro \\ HKEY \_ local \_ Machine \\ software \\ classes. Extension.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-169">Check whether the extension for the type of files that are filtered has a persistent handler registered under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.extension.</span></span> <span data-ttu-id="a7cf1-170">Si es así, deje que esta clave sea {PersistentHandlerGUID}.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-170">If so, let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. <span data-ttu-id="a7cf1-171">Si no hay un controlador persistente registrado para la extensión, busque el CLSID asociado con el tipo de documento en la entrada del registro \\ HKEY \_ local \_ Machine \\ software \\ classes.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-171">If there is not a persistent handler registered for the extension, find the CLSID associated with the document type under the registry entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes.</span></span> <span data-ttu-id="a7cf1-172">Permita que esta clave sea {ApplicationGUID}.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-172">Let this key be {ApplicationGUID}.</span></span> <span data-ttu-id="a7cf1-173">Después, determine si un controlador persistente está registrado para el CLSID: mediante {ApplicationGUID} busque el controlador persistente para la \\ \_ entrada HKEY local \_ Machine \\ software \\ classes \\ CLSID \\ {ApplicationGUID}.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-173">Then determine whether a persistent handler is registered for the CLSID: using {ApplicationGUID} locate the persistent handler for the \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{ApplicationGUID} entry.</span></span> <span data-ttu-id="a7cf1-174">Permita que esta clave sea {PersistentHandlerGUID}.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-174">Let this key be {PersistentHandlerGUID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                (Default) = Class for WWW HTML files
                CLSID
                   (Default) = {25336920-03F9-11CF-8FD0-00AA00686F13}
             CLSID
                {25336920-03F9-11CF-8FD0-00AA00686F13}
                   PersistentHandler
                      (Default) = {PersistentHandlerGUID}
```

3. <span data-ttu-id="a7cf1-175">Determine el GUID del controlador persistente: mediante {PersistentHandlerGUID} busque el GUID del controlador persistente para el tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-175">Determine the GUID of the persistent handler: using {PersistentHandlerGUID} find the persistent handler GUID for the document type.</span></span> <span data-ttu-id="a7cf1-176">El valor de la entrada del registro HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID \\ {PERSISTENTHANDLERGUID} \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF produce el GUID del controlador persistente para este tipo de documento.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-176">The value under the registry entry HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{PersistentHandlerGUID}\\PersistentAddinsRegistered\\ 89BCB740-6119-101A-BCB7-00DD010655AF yields the persistent handler GUID for this document type.</span></span> <span data-ttu-id="a7cf1-177">Permita que esta clave sea {FilterHandlerCLSID}.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-177">Let this key be {FilterHandlerCLSID}.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. <span data-ttu-id="a7cf1-178">Determinar el controlador de filtro: mediante {FilterHandlerCLSID} que se determinó en el paso anterior, busque el controlador de filtro en la entrada \\ HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID \\ {FilterHandlerCLSID} \\ InProcServer32.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-178">Determine the filter handler: using {FilterHandlerCLSID} that was determined in the previous step locate the filter handler under the entry \\HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID\\{FilterHandlerCLSID}\\InprocServer32.</span></span> <span data-ttu-id="a7cf1-179">En este ejemplo, el nombre de controlador de filtro descriptivo usado es HTML IFilter.</span><span class="sxs-lookup"><span data-stu-id="a7cf1-179">In this example the descriptive filter handler name used is HTML IFilter.</span></span>

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             CLSID
                {EEC97550-47A9-11CF-B952-00AA0051FE20}
                   (Default) = HTML IFilter
                    Data type  REG_SZ
                    InprocServer32
                    nlhtml.dll
```

## <a name="additional-resources"></a><span data-ttu-id="a7cf1-180">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="a7cf1-180">Additional Resources</span></span>

- <span data-ttu-id="a7cf1-181">En el ejemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), se muestra cómo crear una clase base de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para implementar la interfaz **IFilter** .</span><span class="sxs-lookup"><span data-stu-id="a7cf1-181">The [IFilterSample](-search-sample-ifiltersample.md) code sample, available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), demonstrates how to create an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) base class for implementing the **IFilter** interface.</span></span>
- <span data-ttu-id="a7cf1-182">Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a7cf1-182">For an overview of the indexing process, see [The Indexing Process](-search-indexing-process-overview.md).</span></span>
- <span data-ttu-id="a7cf1-183">Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="a7cf1-183">For an overview of file types, see [File Types](../shell/fa-file-types.md).</span></span>
- <span data-ttu-id="a7cf1-184">Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a7cf1-184">To query file association attributes for a file type, see [PerceivedTypes, SystemFileAssociations, and Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7cf1-185">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a7cf1-185">Related topics</span></span>

[<span data-ttu-id="a7cf1-186">Desarrollar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="a7cf1-186">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

[<span data-ttu-id="a7cf1-187">Acerca de los controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="a7cf1-187">About Filter Handlers in Windows Search</span></span>](-search-ifilter-about.md)

[<span data-ttu-id="a7cf1-188">Prácticas recomendadas para crear controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="a7cf1-188">Best Practices for Creating Filter Handlers in Windows Search</span></span>](-search-3x-wds-extidx-filters.md)

[<span data-ttu-id="a7cf1-189">Devolver propiedades de un controlador de filtro</span><span class="sxs-lookup"><span data-stu-id="a7cf1-189">Returning Properties from a Filter Handler</span></span>](-search-ifilter-property-filtering.md)

[<span data-ttu-id="a7cf1-190">Controladores de filtro que se distribuyen con Windows</span><span class="sxs-lookup"><span data-stu-id="a7cf1-190">Filter Handlers that Ship with Windows</span></span>](-search-ifilter-implementations.md)

[<span data-ttu-id="a7cf1-191">Implementar controladores de filtro en Windows Search</span><span class="sxs-lookup"><span data-stu-id="a7cf1-191">Implementing Filter Handlers in Windows Search</span></span>](-search-ifilter-constructing-filters.md)

[<span data-ttu-id="a7cf1-192">Probar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="a7cf1-192">Testing Filter Handlers</span></span>](-search-ifilter-testing-filters.md)
