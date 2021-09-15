---
description: Uso de extensiones de Shell para implementar un controlador de enlace de copia.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Cómo crear controladores de enlace de copia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579572"
---
# <a name="how-to-create-copy-hook-handlers"></a>Cómo crear controladores de enlace de copia

Los procedimientos generales para implementar y registrar un controlador de extensión de Shell se de abordan en [Crear controladores de extensión de shell](handlers.md). Este documento se centra en los aspectos de implementación específicos de los controladores de enlace de copia.

-   [Implementar controladores de enlace de copia](#step-1-implementing-copy-hook-handlers)
-   [Registro de controladores de enlace de copia](#step-2-registering-copy-hook-handlers)
-   [Temas relacionados](#related-topics)

## <a name="instructions"></a>Instructions

### <a name="step-1-implementing-copy-hook-handlers"></a>Paso 1: Implementar controladores de enlace de copia

Al igual que todos los controladores de extensión de Shell, los controladores de enlace de copia son objetos del Modelo de objetos componentes (COM) en proceso implementados como archivos DLL. Exportan una interfaz además de [**IUnknown:**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)). El shell inicializa el controlador directamente, por lo que no es necesario una interfaz de inicialización como [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).

La [**interfaz ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) tiene un único método, [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)). Cuando una carpeta está a punto de moverse, shell llama a este método. Pasa una variedad de información, entre las que se incluyen:

-   Nombre de la carpeta.
-   El destino de la carpeta o el nuevo nombre.
-   Operación que se está intentando.
-   Atributos de las carpetas de origen y destino.
-   Identificador de ventana que se puede usar para mostrar una interfaz de usuario.

Cuando se llama al método [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) del controlador, devuelve uno de los tres valores siguientes para indicar al Shell cómo debe continuar.



| Value    | Descripción                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| IDYES    | Permite la operación.                                                                                                                            |
| IDNO     | Impide la operación en esta carpeta. El Shell puede continuar con cualquier otra operación que se haya aprobado, como una operación de copia por lotes. |
| IDCANCEL | Impide la operación actual y cancela las operaciones pendientes.                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a>Paso 2: Registrar controladores de enlace de copia

Los controladores de enlace de copia de las carpetas se registran en la subclave **\_ \_** \\  \\  \\ **CopyHookHandlers** del shell del directorio RAÍZ HKEY CLASSES. Cree una subclave **de CopyHookHandlers** denominada para el controlador y establezca el valor predeterminado de la subclave en la forma de cadena del GUID del identificador de clase (CLSID) del controlador.

En el ejemplo siguiente se agrega la subclave **MyCopyHandler** a la lista de controladores de enlace de copia del shell.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

Los controladores de enlace de copia para objetos de impresora se registran básicamente de la misma manera. La única diferencia es que debe registrarlos en la subclave **HKEY \_ CLASSES \_ ROOT** \\ **Printers.**

## <a name="remarks"></a>Observaciones

Normalmente, los usuarios y las aplicaciones pueden copiar, mover, eliminar o cambiar el nombre de carpetas con pocas restricciones. Al implementar un controlador de enlace de copia, puede controlar si estas operaciones tienen lugar. Por ejemplo, la implementación de este tipo de controlador permite evitar que se cambie el nombre o la eliminación de carpetas críticas. Los controladores de enlace de copia también se pueden implementar para objetos de impresora.

Los controladores de enlace de copia son globales. El Shell llama a todos los controladores registrados cada vez que una aplicación o usuario intenta copiar, mover, eliminar o cambiar el nombre de una carpeta o un objeto de impresora. El controlador no realiza la operación en sí. Solo lo aprueba o veta. Si todos los controladores lo aprueban, el Shell realiza la operación. Si algún controlador veta la operación, se cancela y no se llama a los controladores restantes. Los controladores de enlace de copia no se informan del éxito o error de la operación, por lo que no se pueden usar para supervisar las operaciones de archivos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de controladores de extensiones de shell](handlers.md)
</dt> <dt>

[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))
</dt> </dl>

 

 
