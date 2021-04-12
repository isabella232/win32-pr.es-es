---
title: Agregar iconos y menús contextuales con extensiones de Shell
description: Puede mejorar la experiencia de los usuarios con la búsqueda de escritorio de Microsoft Windows (WDS) y el controlador de protocolo mediante la implementación de extensiones de Shell.
ms.assetid: 899f3fd1-1ae9-45fe-ae6d-26d4f07bf6e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adbd6b0f4c647c47e11d14aea5e5af748a59ba53
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/19/2020
ms.locfileid: "104270763"
---
# <a name="adding-icons-and-context-menus-with-shell-extensions"></a>Agregar iconos y menús contextuales con extensiones de Shell

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

Puede mejorar la experiencia de los usuarios con la búsqueda de escritorio de Microsoft Windows (WDS) y el controlador de protocolo mediante la implementación de extensiones de Shell. Sin extensión adicional, el controlador de protocolo que cree no incluirá las siguientes experiencias de usuario:

-   WDS no mostrará iconos específicos para los resultados.
-   Cuando los usuarios hacen doble clic en un elemento, la interfaz de usuario no responderá al evento.
-   Cuando los usuarios hacen clic con el botón secundario en un elemento, el menú contextual no será compatible con las operaciones del elemento.

Las implementaciones mínimas de **IPersist** y **IPersistFolder** son necesarias para **IShellFolder**, y se requiere una implementación mínima de **IShellFolder** para **IContextMenu** y **IExtractIcon**, las dos interfaces que proporcionan una experiencia de usuario más sencilla.

 

## <a name="ipersist"></a>IPersist

La interfaz **IPersist** define el único método **GetClassID**, que está diseñado para proporcionar el CLSID de un objeto que se puede almacenar de forma persistente en el sistema.



| Método       | Descripción                                 |
|--------------|---------------------------------------------|
| GetClassID () | Devuelve el ClassID del controlador de protocolo. |



 

> [!Note]
>
> Se debe implementar el mismo CLSID para **IPersist**, **IPersistFolder** y **IShellFolder**.

 

 

## <a name="ipersistfolder"></a>IPersistFolder

La interfaz **IPersistFolder** se usa para inicializar los objetos de la carpeta de Shell. La implementación de esta interfaz, que se deriva de **IPersist**, es cómo se indica a la carpeta dónde se encuentra en el espacio de nombres del shell.



| Método       | Descripción                                                                                            |
|--------------|--------------------------------------------------------------------------------------------------------|
| Initialize () | Indica a un objeto de carpeta de Shell que se inicialice a sí mismo basándose en la información que se pasa y devuelve S \_ correctos. |



 

> [!Note]
>
> Se debe implementar el mismo CLSID para **IPersist**, **IPersistFolder** y **IShellFolder**.

 

No utilice esta interfaz directamente. Lo usa la implementación del sistema de archivos de la interfaz IShellFolder:: BindToObject cuando Inicializa un objeto de carpeta de Shell.

 

## <a name="ishellfolder"></a>IShellFolder

La interfaz **IShellFolder** se usa para administrar carpetas y se requiere una implementación parcial para que las interfaces de icono y de contexto implementadas para un controlador de protocolo se comporten correctamente en la interfaz de usuario de los resultados de búsqueda de escritorio de Windows. La mayor parte de la funcionalidad requerida se expone a través del método **GetUIObjectOf** . Este método permite que un complemento consulte las interfaces **IExtractIcon** y **IContextMenu** .

La interfaz **IShellFolder** utiliza PIDL en lugar de direcciones URL. A diferencia de los requisitos de una extensión de espacio de nombres completa, los complementos pueden usar una estructura IDL simple que solo contenga la dirección URL.

Se deben implementar los siguientes métodos de **IShellFolder** . Tenga en cuenta que cinco de estos métodos requieren una implementación mínima.



| Método             | Descripción                                                                                                                                                                                                 |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BindToObject()     | Devuelve E \_ NOTIMPL                                                                                                                                                                                          |
| BindToStorage()    | Devuelve E \_ NOTIMPL                                                                                                                                                                                          |
| CreateViewObject() | Devuelve E \_ NOTIMPL                                                                                                                                                                                          |
| SetNameOf()        | Devuelve E \_ NOTIMPL                                                                                                                                                                                          |
| ParseDisplayName() | Convierte una dirección URL en la estructura PIDL                                                                                                                                                                        |
| CompareIDs()       | Compara dos valores de PIDL                                                                                                                                                                                    |
| GetDisplayNameOf() | Devuelve la dirección URL de un PIDL                                                                                                                                                                                  |
| GetUIObjectOf()    | Este método es similar al método QueryInterface de OLE COM. Si se solicita un icono, el autor de la llamada solicita el IID \_ IExtractIcon; si se solicita un menú contextual, el autor de la llamada solicita el IID \_ IContextMenu. |



 

> [!Note]
>
> Se debe implementar el mismo CLSID para **IPersist**, **IPersistFolder** y **IShellFolder**.

 

**IShellFolder** no se utiliza para enumerar carpetas. Esto significa que el nombre para mostrar de una carpeta será la dirección URL física. Esto puede cambiar en el futuro.

 

## <a name="icontextmenu"></a>IContextMenu

Cuando WDS muestra los resultados al usuario, puede hacer clic con el botón secundario en un elemento y ver un menú contextual definido por la interfaz **IContextMenu** .

La acción predeterminada en el menú contextual es la misma acción que se realiza cuando se hace doble clic en el elemento. Sin las interfaces de **IShellFolder** o **IContextMenu** correspondientes para el elemento, el comportamiento predeterminado para un evento de doble clic es pasar la dirección URL como un argumento a la función ShellExecute.

 

## <a name="iextracticon"></a>IExtractIcon

**IExtractIcon** recupera un icono para la interfaz de usuario de WDS basado en la dirección URL en el PIDL proporcionado por el controlador de protocolo.

 

## <a name="code-sample"></a>Ejemplo de código

En el código de ejemplo de la [interfaz de usuario del controlador de protocolo personalizado](-search-2x-wds-ph-ui-samplecode.md) se muestra una implementación de **IShellFolder** y las interfaces auxiliares, e incluye compatibilidad para manipular el PIDL.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Código de ejemplo de la interfaz de usuario del controlador de protocolo personalizado](-search-2x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Instalar y registrar controladores de protocolo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 




