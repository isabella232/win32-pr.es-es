---
description: Usar las extensiones de Shell para implementar un controlador de enlace de copia.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Cómo crear controladores de enlace de copia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276751"
---
# <a name="how-to-create-copy-hook-handlers"></a>Cómo crear controladores de enlace de copia

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se explican en [crear controladores de extensión de Shell](handlers.md). Este documento se centra en los aspectos de la implementación que son específicos de los controladores de enlace de copia.

-   [Implementar controladores de enlace de copia](#step-1-implementing-copy-hook-handlers)
-   [Registrando controladores de enlace de copia](#step-2-registering-copy-hook-handlers)
-   [Temas relacionados](#related-topics)

## <a name="instructions"></a>Instrucciones

### <a name="step-1-implementing-copy-hook-handlers"></a>Paso 1: implementación de controladores de enlace de copia

Al igual que todos los controladores de extensión de Shell, los controladores de enlace de copia son objetos de modelo de objetos componentes (COM) en proceso implementados como archivos dll. Exportan una interfaz además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)). El shell inicializa el controlador directamente, por lo que no hay necesidad de una interfaz de inicialización como [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).

La interfaz [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) tiene un único método, [**ICopyHook:: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)). Cuando se va a migrar una carpeta, el shell llama a este método. Pasa una gran variedad de información, entre las que se incluyen:

-   Nombre de la carpeta.
-   El destino de la carpeta o el nuevo nombre.
-   Operación que se está intentando.
-   Los atributos de las carpetas de origen y de destino.
-   Identificador de ventana que se puede utilizar para mostrar una interfaz de usuario.

Cuando se llama al método [**ICopyHook:: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) del controlador, devuelve uno de los tres valores siguientes para indicar al shell cómo debe continuar.



| Value    | Descripción                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| IDYES    | Permite la operación.                                                                                                                            |
| IDNO     | Impide la operación en esta carpeta. El shell puede continuar con cualquier otra operación que se haya aprobado, como una operación de copia por lotes. |
| IDCANCEL | Evita la operación actual y cancela las operaciones pendientes.                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a>Paso 2: registrar controladores de enlace de copia

Los controladores de enlace de copia para las carpetas se registran en la subclave del directorio **\_ \_ raíz de las clases HKEY** \\  \\ **shellex** \\ **CopyHookHandlers** . Cree una subclave de **CopyHookHandlers** denominada para el controlador y establezca el valor predeterminado de la subclave en la forma de cadena del GUID del identificador de clase (CLSID) del controlador.

En el ejemplo siguiente se agrega la subclave **MyCopyHandler** a la lista de controladores del enlace de copia del shell.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

Los controladores de enlace de copia para objetos de impresora se registran esencialmente de la misma manera. La única diferencia es que debe registrarlos en la subclave de **\_ las impresoras \_ raíz de las clases HKEY** \\  .

## <a name="remarks"></a>Observaciones

Normalmente, los usuarios y las aplicaciones pueden copiar, trasladar, eliminar o cambiar el nombre de las carpetas con pocas restricciones. Mediante la implementación de un controlador de enlace de copia, puede controlar si estas operaciones tienen lugar. Por ejemplo, la implementación de este tipo de controlador le permite evitar que las carpetas críticas se cambien de nombre o se eliminen. Los controladores de enlace de copia también se pueden implementar para objetos de impresora.

Los controladores de enlace de copia son globales. El shell llama a todos los controladores registrados cada vez que una aplicación o un usuario intenta copiar, quitar, eliminar o cambiar el nombre de una carpeta o un objeto de impresora. El controlador no realiza la operación en sí. Solo lo aprueba o lo veta. Si todos los controladores aprueban, el shell realiza la operación. Si un controlador veta la operación, se cancela y no se llama a los controladores restantes. Los controladores de enlace de copia no se informan de si la operación se ha realizado correctamente o no, por lo que no se pueden usar para supervisar las operaciones de archivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de controladores de extensiones de shell](handlers.md)
</dt> <dt>

[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))
</dt> </dl>

 

 
