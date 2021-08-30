---
description: El controlador de filtro debe estar registrado. También puede buscar un controlador de filtro existente para una extensión de nombre de archivo determinada a través del Registro o mediante la interfaz ILoadFilter.
ms.assetid: 3478b948-73c7-4533-974a-d9b5186a651b
title: Registro de controladores de filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ffaf53cc62f5f8647bbded05761e43a6cff97a48d8dc2006d1bfafe9da45a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058145"
---
# <a name="registering-filter-handlers"></a>Registro de controladores de filtro

El controlador de filtro debe estar registrado. También puede buscar un controlador de filtro existente para una extensión de nombre de archivo determinada a través del Registro o mediante la [**interfaz ILoadFilter.**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter)

Este tema se organiza de la siguiente manera:

- [Registrar controladores de filtros para la Windows búsqueda](#registering-filter-handlers)
  - [Enfoque obsoleto para registrar controladores de filtros](#obsolete-approach-for-registering-filters-handlers)
- [Reemplazar controladores de filtro existentes](#replacing-existing-filter-handlers)
- [Buscar un controlador de filtros para una extensión de archivo determinada](#finding-a-filter-handler-for-a-given-file-extension)
- [Recursos adicionales](#additional-resources)
- [Temas relacionados](#related-topics)

> [!NOTE]  
> Un controlador de filtro es una implementación de la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter)

## <a name="registering-filters-handlers-for-windows-search"></a>Registrar controladores de filtros para la Windows búsqueda

Los GUID que necesita para registrar un nuevo controlador de protocolo o para buscar un controlador de protocolo existente se enumeran en la tabla siguiente.

| GUID                                     | Usuario o aplicación definidos | Descripción                                                                                               |
|------------------------------------------|-----------------------------|-----------------------------------------------------------------------------------------------------------|
| **89BCB740-6119-101A-BCB7-00DD010655AF** | Application                 | El GUID de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) es una constante de clave del Registro para todos los controladores de filtro. |
| **{PersistentHandlerGUID}**              | Usuario                        | Este es el GUID del controlador persistente.                                                              |
| **{FilterHandlerCLSID}**                 | Usuario                        | Este es el identificador de clase (CLSID) para el controlador de filtro.                                              |
| **{ApplicationGUID}**                    | Usuario                        | Se trata de un GUID intermedio (agregado).                                                                |

Los controladores de filtro deben registrarse en HKEY LOCAL MACHINE porque SearchFilterHost.exe se ejecuta en la cuenta SYSTEM y, por tanto, no puede acceder a las claves del Registro para HKEY CURRENT USER para el usuario que ha iniciado \_ \_ \_ \_ sesión. Además, el grupo Usuarios debe tener acceso de lectura y ejecución al controlador de filtro .dll porque SearchFilterHost.exe quita todos los derechos de administrador y solo permite derechos que no son de administrador. Dado que la ubicación predeterminada del proyecto Visual Studio está en el directorio del usuario actual y, por tanto, no concede permisos de lectura al grupo Usuarios, debe mover el .dll o cambiar las ACL para permitir el acceso SearchFilterHost.exe.

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

2. Registre el controlador de filtro con las siguientes claves y valores:

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

Este enfoque no se recomienda para su uso. Los filtros se pueden registrar para un CLSID que representa una clase de Modelo de objetos componentes (COM) o para una extensión de nombre de archivo. Puede registrar ambos filtros si necesita registrar un controlador de filtro para una clase y un controlador de filtro diferente para una extensión de nombre de archivo dentro de la clase . Tenga en cuenta que un controlador de filtro registrado para una extensión de nombre de archivo tiene prioridad sobre un controlador de filtro para un CLSID.

Estas entradas son entradas estándar del Registro OLE hasta e incluyen la entrada de la clase **CLSID \\ {ApplicationGUID}.** El archivo DLL sample.dll el comportamiento del objeto en ejecución para la .txt clase . Tenga en cuenta la entrada adicional PersistentHandler. Esta entrada especifica la clase responsable de la intermediación de solicitudes a los objetos persistentes de la clase de ejemplo. La entrada de **PersistentAddinsRegistered** identifica la implementación responsable de la interfaz denominada **89BCB740-6119-101A-BCB7-00DD010655AF**(IID \_ IFilter). La clase que implementa **IID \_ IFilter tiene** entradas del Registro OLE estándar. El archivo DLL InprocServer32 se carga a través del mecanismo OLE estándar.

Windows La búsqueda observa el modelo de subprocesos especificado para el controlador de filtro. Cuando el modelo de subprocesos se establece en **Ambos**, el controlador de filtro debe ser seguro para subprocesos; De lo contrario, si no es seguro para subprocesos, especifique **Apartment**. Tenga en cuenta que los controladores de filtro siempre deben ser seguros para subprocesos.

Las siguientes entradas del Registro de ejemplo son para un controlador de filtro registrado para una extensión de nombre de archivo y clase. **{PersistentHandlerGUID}** y **{FilterHandlerCLSID}** se usan como variables que indican valores que el creador del controlador de filtros debe especificar. Los valores son de tipo REG \_ SZ.

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

Se recomienda no reemplazar los controladores de filtro integrados para tipos de archivo comunes como .txt, .doc, .html, .url, etc., ya que puede tener efectos no deseados en otros componentes del sistema. La indexación de cuerpos de mensajes de correo electrónico depende de .txt, .html y controladores de filtro .rtf, por ejemplo.

Si se instala un nuevo controlador de filtro para un tipo de archivo como reemplazo de un registro de filtro existente, el instalador debe guardar el registro actual y restaurarlo si se desinstala el nuevo controlador de filtros. No hay ningún mecanismo para encadenar filtros. Por lo tanto, el nuevo controlador de filtro es responsable de replicar cualquier funcionalidad necesaria del filtro anterior.

## <a name="finding-a-filter-handler-for-a-given-file-extension"></a>Buscar un controlador de filtros para una extensión de archivo determinada

Puede usar la interfaz [**ILoadFilter para**](/windows/desktop/api/filtereg/nn-filtereg-iloadfilter) buscar un controlador de filtro para una extensión de nombre de archivo determinada. En las siguientes entradas del Registro de ejemplo se muestra cómo hacerlo para los archivos HTML. En este ejemplo, el controlador de filtros para documentos HTML es nlhtml.dll. Los valores son de tipo REG \_ SZ.

**Para buscar el controlador de filtro para una extensión de nombre de archivo determinada:**

1. Compruebe si la extensión para el tipo de archivos filtrados tiene un controlador persistente registrado en la entrada del Registro \\ HKEY \_ LOCAL MACHINE SOFTWARE \_ \\ \\ Classes.extension. Si es así, deje que esta clave sea {PersistentHandlerGUID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {PersistentHandlerGUID}
```

2. Si no hay ningún controlador persistente registrado para la extensión, busque el CLSID asociado al tipo de documento en la entrada del Registro HKEY LOCAL MACHINE SOFTWARE Classes (Clases de SOFTWARE de \\ HKEY \_ LOCAL \_ \\ \\ MACHINE). Deje que esta clave sea {ApplicationGUID}. A continuación, determine si se registra un controlador persistente para el CLSID: mediante {ApplicationGUID} busque el controlador persistente para la entrada \\ \_ \_ \\ \\ \\ CLSID \\ {ApplicationGUID} de las clases DE SOFTWARE HKEY LOCAL MACHINE. Deje que esta clave sea {PersistentHandlerGUID}.

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

3. Determine el GUID del controlador persistente: mediante {PersistentHandlerGUID} busque el GUID del controlador persistente para el tipo de documento. El valor de la entrada del Registro HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ CLSID \\ {PersistentHandlerGUID} \\ PersistentAddinsRegistered \\ 89BCB740-6119-101A-BCB7-00DD010655AF produce el GUID del controlador persistente para este tipo de documento. Deje que esta clave sea {FilterHandlerCLSID}.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {PersistentHandlerGUID}
                (Default) = HTML File Persistent Handler<dl>
                    REG_SZ     {89BCB740-6119-101A-BCB7-00DD010655AF}
                    REG_SZ     (Default) = {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. Determine el controlador de filtro: mediante {FilterHandlerCLSID} que se determinó en el paso anterior, busque el controlador de filtro en la entrada \\ HKEY \_ LOCAL MACHINE SOFTWARE Classes \_ \\ \\ \\ CLSID \\ {FilterHandlerCLSID} \\ InprocServer32. En este ejemplo, el nombre descriptivo del controlador de filtro utilizado es HTML IFilter.

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

- El [ejemplo de código IFilterSample,](-search-sample-ifiltersample.md) disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), muestra cómo crear una clase base [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para implementar la **interfaz IFilter.**
- Para obtener información general sobre el proceso de indexación, vea [El proceso de indexación](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, vea [Tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de asociación de archivos para un tipo de archivo, vea [PerceivedTypes, SystemFileAssociations y Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

[Acerca de los controladores de filtro en Windows Search](-search-ifilter-about.md)

[Procedimientos recomendados para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md)

[Devolver propiedades de un controlador de filtros](-search-ifilter-property-filtering.md)

[Controladores de filtro que se envían con Windows](-search-ifilter-implementations.md)

[Implementación de controladores de filtro en Windows Search](-search-ifilter-constructing-filters.md)

[Probar controladores de filtro](-search-ifilter-testing-filters.md)
