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
# <a name="registering-filter-handlers"></a>Registrar controladores de filtro

El controlador de filtro debe estar registrado. También puede buscar un controlador de filtro existente para una extensión de nombre de archivo determinada a través del registro o mediante la interfaz [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) .

Este tema se organiza de la siguiente manera:

- [Registro de controladores de filtros para Windows Search](#registering-filter-handlers)
  - [Enfoque obsoleto para registrar controladores de filtros](#obsolete-approach-for-registering-filters-handlers)
- [Reemplazar controladores de filtro existentes](#replacing-existing-filter-handlers)
- [Buscar un controlador de filtro para una extensión de archivo determinada](#finding-a-filter-handler-for-a-given-file-extension)
- [Recursos adicionales](#additional-resources)
- [Temas relacionados](#related-topics)

> [!NOTE]  
> Un controlador de filtro es una implementación de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .

## <a name="registering-filters-handlers-for-windows-search"></a>Registro de controladores de filtros para Windows Search

En la tabla siguiente se enumeran los GUID necesarios para registrar un nuevo controlador de protocolo o para buscar un controlador de protocolo existente.

| GUID                                     | Definido por el usuario o la aplicación | Descripción                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| **89BCB740-6119-101A-BCB7-00DD010655AF** | Application                 | El GUID de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) es una constante de clave del registro para todos los controladores de filtro. |
| **{PersistentHandlerGUID}**              | User (Usuario)                        | Este es el GUID del controlador persistente.                                                              |
| **{FilterHandlerCLSID}**                 | User (Usuario)                        | Este es el identificador de clase (CLSID) para el controlador de filtro.                                              |
| **{ApplicationGUID}**                    | User (Usuario)                        | Se trata de un GUID intermedio (agregado).                                                                |

Los controladores de filtro deben estar registrados en \_ \_ el equipo local hkey porque SearchFilterHost.exe se está ejecutando en la cuenta del sistema y, por tanto, no pueden tener acceso a las claves del registro para \_ el usuario actual de HKEY \_ para el usuario que ha iniciado sesión. Además, el grupo de usuarios debe tener acceso de lectura y ejecución al controlador de filtro. dll porque SearchFilterHost.exe quita todos los derechos de administrador y solo permite derechos que no son de administrador. Dado que la ubicación predeterminada del proyecto de Visual Studio se encuentra en el directorio del usuario actual y, por tanto, no concede permisos de lectura al grupo de usuarios, debe trasladar el archivo. dll o cambiar las ACL para permitir el acceso a SearchFilterHost.exe.

Al registrar un nuevo controlador de filtro, se recomienda usar un nombre descriptivo, por ejemplo, HTML IFilter.

**Para registrar el nuevo controlador de filtro:**

1. Especifique la extensión y el GUID del controlador persistente que usará el controlador de filtro:

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

2. Registre el controlador de filtro con las claves y los valores siguientes:

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

### <a name="obsolete-approach-for-registering-filters-handlers"></a>Enfoque obsoleto para registrar controladores de filtros

Este enfoque no se recomienda para su uso. Los filtros se pueden registrar para un CLSID que representa una clase de modelo de objetos componentes (COM) y/o para una extensión de nombre de archivo. Podría registrar ambos filtros si necesita registrar un controlador de filtro para una clase y un controlador de filtro diferente para una extensión de nombre de archivo dentro de la clase. Tenga en cuenta que un controlador de filtro registrado para una extensión de nombre de archivo tiene prioridad sobre un controlador de filtro para un CLSID.

Estas entradas son entradas del registro OLE estándar hasta la entrada de la clase **CLSID \\ {ApplicationGUID}**, inclusive. El sample.dll DLL implementa el comportamiento del objeto en ejecución para la clase. txt. Observe la entrada adicional, PersistentHandler. Esta entrada especifica la clase responsable de las solicitudes de agente a los objetos persistentes de la clase de ejemplo. La entrada en **PersistentAddinsRegistered** identifica la implementación responsable de la interfaz denominada **89BCB740-6119-101A-BCB7-00DD010655AF**(IID \_ IFilter). La clase que implementa el **\_ IFilter de IID** tiene entradas de registro estándar de OLE. La DLL InprocServer32 se carga a través del mecanismo estándar de OLE.

Windows Search observa el modelo de subprocesos especificado para el controlador de filtro. Cuando el modelo de subprocesos se establece en **ambos**, el controlador de filtro debe ser seguro para subprocesos; de lo contrario, si no es seguro para subprocesos, especifique **Apartment**. Tenga en cuenta que los controladores de filtro siempre deben ser seguros para subprocesos.

Las siguientes entradas del registro de ejemplo son para un controlador de filtro registrado para una extensión de nombre de archivo y una clase. **{PersistentHandlerGUID}** y **{FilterHandlerCLSID}** se usan como variables que indican valores que deben ser especificados por el creador del controlador de filtro. Los valores son de tipo REG \_ SZ.

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

## <a name="replacing-existing-filter-handlers"></a>Reemplazar controladores de filtro existentes

Se recomienda no reemplazar los controladores de filtro integrados para los tipos de archivo comunes, como. txt,. doc,. html,. URL, etc., ya que esto puede tener efectos no deseados en otros componentes del sistema. La indexación de cuerpos de mensaje de correo electrónico depende de los controladores de filtro. txt,. html y. rtf, por ejemplo.

Si se va a instalar un nuevo controlador de filtro para un tipo de archivo como sustituto de un registro de filtro existente, el instalador debe guardar el registro actual y restaurarlo si se desinstala el nuevo controlador de filtro. No hay ningún mecanismo para encadenar filtros. Por lo tanto, el nuevo controlador de filtro es responsable de replicar cualquier funcionalidad necesaria del filtro antiguo.

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a>Buscar un controlador de filtro para una extensión de archivo determinada

Puede usar la interfaz [**ILoadFilter**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) para buscar un controlador de filtro para una extensión de nombre de archivo determinada. En las entradas del registro de ejemplo siguiente se muestra cómo hacerlo para los archivos HTML. En este ejemplo, el controlador de filtro para documentos HTML es nlhtml.dll. Los valores son de tipo REG \_ SZ.

**Para buscar el controlador de filtro para una extensión de nombre de archivo determinada:**

1. Compruebe si la extensión del tipo de archivos filtrados tiene un controlador persistente registrado en la entrada del registro \\ HKEY \_ local \_ Machine \\ software \\ classes. Extension. Si es así, deje que esta clave sea {PersistentHandlerGUID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. Si no hay un controlador persistente registrado para la extensión, busque el CLSID asociado con el tipo de documento en la entrada del registro \\ HKEY \_ local \_ Machine \\ software \\ classes. Permita que esta clave sea {ApplicationGUID}. Después, determine si un controlador persistente está registrado para el CLSID: mediante {ApplicationGUID} busque el controlador persistente para la \\ \_ entrada HKEY local \_ Machine \\ software \\ classes \\ CLSID \\ {ApplicationGUID}. Permita que esta clave sea {PersistentHandlerGUID}.

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

3. Determine el GUID del controlador persistente: mediante {PersistentHandlerGUID} busque el GUID del controlador persistente para el tipo de documento. El valor de la entrada del registro HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID \\ {PERSISTENTHANDLERGUID} \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF produce el GUID del controlador persistente para este tipo de documento. Permita que esta clave sea {FilterHandlerCLSID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. Determinar el controlador de filtro: mediante {FilterHandlerCLSID} que se determinó en el paso anterior, busque el controlador de filtro en la entrada \\ HKEY \_ local \_ Machine \\ software \\ classes \\ CLSID \\ {FilterHandlerCLSID} \\ InProcServer32. En este ejemplo, el nombre de controlador de filtro descriptivo usado es HTML IFilter.

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

## <a name="additional-resources"></a>Recursos adicionales

- En el ejemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), se muestra cómo crear una clase base de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para implementar la interfaz **IFilter** .
- Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

[Acerca de los controladores de filtro en Windows Search](-search-ifilter-about.md)

[Prácticas recomendadas para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md)

[Devolver propiedades de un controlador de filtro](-search-ifilter-property-filtering.md)

[Controladores de filtro que se distribuyen con Windows](-search-ifilter-implementations.md)

[Implementar controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md)

[Probar controladores de filtro](-search-ifilter-testing-filters.md)
