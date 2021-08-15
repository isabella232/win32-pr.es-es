---
title: Agregar iconos y menús contextuales con extensiones de shell
description: Puede mejorar la experiencia de los usuarios con Microsoft Windows Desktop Search (WDS) y el controlador de protocolos mediante la implementación de extensiones de Shell.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9198fc56b8ca09e61909b1828d7d00b964bb12c0e13308583eb36a4e2211f3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976875"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a>Agregar iconos y menús contextuales con extensiones de shell

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

Puede mejorar la experiencia de los usuarios con Microsoft Windows Desktop Search (WDS) y el controlador de protocolos mediante la implementación de extensiones de Shell. Sin más extensión, el controlador de protocolo que cree no incluirá las siguientes experiencias de usuario:

-   WDS no mostrará iconos específicos para los resultados.
-   Cuando los usuarios hacen doble clic en un elemento, la interfaz de usuario no responderá al evento.
-   Cuando los usuarios hacen clic con el botón derecho en un elemento, el menú contextual no admitirá ninguna operación para el elemento.

**IShellFolder** requiere implementaciones mínimas de **IPersist** e **IPersistFolder,** y se requiere una implementación mínima de **IShellFolder** para **IContextMenu** e **IExtractIcon,** las dos interfaces que proporcionan una experiencia de usuario más fluida.

 

## <a name="ipersist"></a>IPersist

La **interfaz IPersist** define el método único **GetClassID**, que está diseñado para proporcionar el CLSID de un objeto que se puede almacenar de forma persistente en el sistema.



| Método       | Descripción                                 |
|--------------|---------------------------------------------|
| GetClassID() | Devuelve el ClassID del controlador de protocolo. |



 

> [!Note]
>
> Se debe implementar el mismo CLSID para **IPersist,** **IPersistFolder** e **IShellFolder.**

 

 

## <a name="ipersistfolder"></a>IPersistFolder

La **interfaz IPersistFolder** se usa para inicializar objetos de carpeta de Shell. La implementación de esta interfaz, que se deriva de **IPersist,** es la forma en que se explica a la carpeta dónde se encuentra en el espacio de nombres de Shell.



| Método       | Descripción                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| Initialize() | Indica a un objeto de carpeta de Shell que se inicialice en función de la información pasada y devuelve S \_ OK |



 

> [!Note]
>
> Se debe implementar el mismo CLSID para **IPersist,** **IPersistFolder** e **IShellFolder.**

 

Esta interfaz no se usa directamente. Lo usa la implementación del sistema de archivos de la interfaz IShellFolder::BindToObject cuando inicializa un objeto de carpeta de Shell.

 

## <a name="ishellfolder"></a>IShellFolder

La interfaz **IShellFolder** se usa para administrar carpetas y se requiere una implementación parcial para que las interfaces de icono y contexto implementadas para un controlador de protocolo se comporten correctamente en la interfaz de usuario de resultados de la búsqueda de escritorio de Windows. La mayor parte de la funcionalidad necesaria se expone a través **del método GetUIObjectOf.** Este método permite que un complemento consulte las interfaces **IExtractIcon** **e IContextMenu.**

La **interfaz IShellFolder** usa PIDL en lugar de direcciones URL. A diferencia de los requisitos de una extensión de espacio de nombres completa, los complementos pueden usar una estructura IDL simple que contiene solo la dirección URL.

Se deben implementar los métodos siguientes de **IShellFolder.** Tenga en cuenta que cinco de estos métodos requieren una implementación mínima.



| Método             | Descripción                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject()     | Devuelve E \_ NOTIMPL                                                                                                                                                                                          |
| BindToStorage()    | Devuelve E \_ NOTIMPL                                                                                                                                                                                          |
| CreateViewObject() | Devuelve E \_ NOTIMPL                                                                                                                                                                                          |
| SetNameOf()        | Devuelve E \_ NOTIMPL                                                                                                                                                                                          |
| ParseDisplayName() | Convierte una dirección URL en la estructura PIDL.                                                                                                                                                                        |
| CompareIDs()       | Compara dos valores PIDL.                                                                                                                                                                                    |
| GetDisplayNameOf() | Devuelve la dirección URL de un PIDL.                                                                                                                                                                                  |
| GetUIObjectOf()    | Este método es similar al método QueryInterface de OLE COM. Si se solicita un icono, el autor de la llamada solicita el IID IExtractIcon; si se solicita un menú contextual, el autor de la llamada solicita el \_ IID \_ IContextMenu. |



 

> [!Note]
>
> Se debe implementar el mismo CLSID para **IPersist,** **IPersistFolder** e **IShellFolder.**

 

**IShellFolder** no se usa para enumerar carpetas. Esto significa que el nombre para mostrar de una carpeta será la dirección URL física. Esto puede cambiar en el futuro.

 

## <a name="icontextmenu"></a>IContextMenu

Cuando WDS muestra los resultados al usuario, el usuario puede hacer clic con el botón derecho en un elemento y ver un menú contextual definido por la **interfaz IContextMenu.**

La acción predeterminada en el menú contextual es la misma que se hace cuando se hace doble clic en el elemento. Sin las interfaces **IShellFolder** o **IContextMenu** correspondientes para el elemento, el comportamiento predeterminado para un evento de doble clic es pasar la dirección URL como argumento a la función ShellExecute.

 

## <a name="iextracticon"></a>IExtractIcon

**IExtractIcon recupera** un icono para la interfaz de usuario de WDS en función de la dirección URL del PIDL proporcionado por el controlador de protocolo.

 

## <a name="code-sample"></a>Ejemplo de código

El [controlador de protocolo personalizado Interfaz de usuario ejemplo](-search-2x-wds-ph-ui-samplecode.md) muestra una implementación de **IShellFolder** y las interfaces de compatibilidad e incluye compatibilidad para manipular las PIDL.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Código de ejemplo de controlador Interfaz de usuario protocolo personalizado](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalación y registro de controladores de protocolo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




