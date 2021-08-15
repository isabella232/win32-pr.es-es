---
description: Muchas Panel de control aplicaciones muestran una hoja de propiedades propiedades para permitir a los usuarios ver y modificar diversas configuraciones del dispositivo y del sistema.
title: Cómo registrar e implementar un controlador de hoja de propiedades para una Panel de control aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6865e8e50aefdea3e3d25c29c9abd3bbbabf5c6af3b770537ed187f8b055bdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859594"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a>Cómo registrar e implementar un controlador de hoja de propiedades para una Panel de control aplicación

Muchas Panel de control aplicaciones muestran una hoja de propiedades propiedades para permitir a los usuarios ver y modificar diversas configuraciones del dispositivo y del sistema. Dos de estas aplicaciones( Mouse y Display) permiten a los controladores de hojas de propiedades reemplazar una o varias de sus páginas por una página personalizada. En la siguiente captura de pantalla se muestra la **hoja de propiedades Propiedades** del mouse.

![hoja de propiedades de propiedades del mouse](images/propsheethandler3.jpg)

Los controladores de hoja de propiedades Panel de control aplicaciones son similares a los de los tipos de archivo, con dos excepciones principales:

-   Una aplicación de Panel de control, no el shell, los llama.
-   Se registran de forma diferente.

## <a name="what-you-need-to-know"></a>Lo que necesita saber

### <a name="technologies"></a>Tecnologías

-   Shell

### <a name="prerequisites"></a>Requisitos previos

-   Descripción de la Panel de control
-   Descripción de los menús contextuales

## <a name="instructions"></a>Instructions

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a>Paso 1: Registrar un controlador de hoja de propiedades para una Panel de control aplicación

Un Panel de control hoja de propiedades de la aplicación debe registrarse en la subclave Panel de control aplicación. Esta clave puede estar en cualquiera de las dos ubicaciones, dependiendo de si el controlador debe ser por usuario o por equipo. Para el registro por usuario, la subclave Panel de control es **HKEY \_ CURRENT \_ USER** \\ **Panel de control**. La macro REGSTR PATH CONTROLPANEL tal como se define en Regstr.h se puede usar en el código en lugar de \_ \_ "Panel de control". Para el registro por equipo, la ubicación es:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

Esta ruta de acceso se puede hacer referencia en el código como HKEY LOCAL MACHINE REGSTR PATH CONTROLSFOLDER, mediante la macro REGSTR PATH CONTROLSFOLDER que se define \_ \_ en \\ \_ \_ \_ \_ Regstr.h.

Las Panel de control que permiten a los controladores de hojas de propiedades reemplazar páginas tienen una subclave bajo la subclave de Panel de control, denominada para la aplicación, como Mouse y Mostrar. La subclave de la aplicación debe tener una **subclave shellex** con una subclave **PropertySheetHandlers.** Para registrar un controlador de hoja de propiedades, agregue su GUID a la subclave **PropertySheetHandlers** que está asociada a la Panel de control aplicación. Para ello, cree una subclave de la subclave **PropertySheetHandlers,** denominada para el controlador de hoja de propiedades, y establezca su valor predeterminado en el formato de cadena del GUID del controlador.

En el ejemplo siguiente se registra un controlador de hoja de propiedades para la aplicación Panel de control mouse por equipo. Para registrarlo por usuario, reemplace **HKEY \_ LOCAL \_ MACHINE** \\ **REGSTR \_ PATH \_ CONTROLSFOLDER** por **HKEY CURRENT \_ \_ USER** \\ **REGSTR \_ PATH \_ CONTROLPANEL**.

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a>Paso 2: Implementar un controlador de hoja de propiedades para una Panel de control aplicación

El procedimiento para implementar un controlador Panel de control hoja de propiedades es muy similar al descrito en Cómo registrar e implementar un controlador de hoja de propiedades para un [tipo de archivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md). La diferencia principal es que [**ahora IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) necesita una implementación notoken en lugar de [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).

Cuando una Panel de control está a punto de mostrar su hoja de propiedades, llama al método [**IShellPropSheetExt::ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) del controlador de la hoja de propiedades una vez para cada página que se pueda reemplazar. El *parámetro uPageID* se establece en el identificador de la página. Los IDs de las páginas disponibles se definen en Cplext.h. Los IDs disponibles actualmente se muestran en la tabla siguiente. 

| Identificador de página                      | Descripción         | Panel de control aplicación |
|------------------------------|---------------------|---------------------------|
| BOTONES DEL MOUSE DE CPLPAGE \_ \_      | Página Botones    | Mouse                     |
| CPLPAGE \_ MOUSE \_ PTRMOTION    | La página Movimiento     | Mouse                     |
| RUEDA DEL MOUSE DE CPLPAGE \_ \_        | Página Rueda      | Mouse                     |
| VELOCIDAD DEL TECLADO DE CPLPAGE \_ \_     | Página Velocidad      | Keyboard                  |
| FONDO DE PRESENTACIÓN DE CPLPAGE \_ \_ | La página Background (Fondo) | Mostrar                   |



 

## <a name="remarks"></a>Comentarios

El procedimiento para crear y reemplazar una página es idéntico al de agregar una página. Para obtener más información, [vea Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).

 

 



