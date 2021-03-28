---
description: Muchas aplicaciones del panel de control muestran una hoja de propiedades para que los usuarios puedan ver y modificar diversas configuraciones del sistema y del dispositivo.
title: Cómo registrar e implementar un controlador de la hoja de propiedades para una aplicación del panel de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909534"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a>Cómo registrar e implementar un controlador de la hoja de propiedades para una aplicación del panel de control

Muchas aplicaciones del panel de control muestran una hoja de propiedades para que los usuarios puedan ver y modificar diversas configuraciones del sistema y del dispositivo. Dos de estas aplicaciones (mouse y pantalla) permiten a los controladores de hojas de propiedades reemplazar una o varias de sus páginas por una página personalizada. En la captura de pantalla siguiente se muestra la hoja de propiedades **del mouse** .

![propiedades del mouse (hoja de propiedades)](images/propsheethandler3.jpg)

Los controladores de la hoja de propiedades de las aplicaciones del panel de control son similares a los de los tipos de archivo, con dos excepciones principales:

-   Los llama una aplicación del panel de control, no el shell.
-   Se registran de forma diferente.

## <a name="what-you-need-to-know"></a>Aspectos que debe saber

### <a name="technologies"></a>Tecnologías

-   Shell

### <a name="prerequisites"></a>Requisitos previos

-   Descripción del panel de control
-   Descripción de los menús contextuales

## <a name="instructions"></a>Instrucciones

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a>Paso 1: registrar un controlador de la hoja de propiedades para una aplicación del panel de control

Un controlador de la hoja de propiedades de la aplicación del panel de control debe estar registrado en la subclave del panel de control. Esta clave puede estar en cualquiera de las dos ubicaciones, en función de si el controlador debe ser por usuario o por equipo. En el caso del registro por usuario, la subclave del panel de control es **HKEY \_ Current \_ User** \\ **control panel**. La macro REGSTR \_ ruta de acceso \_ CONTROLPANEL tal y como se define en REGSTR. h puede usarse en el código en lugar del "panel de control". En el caso del registro por equipo, la ubicación es:

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

Se puede hacer referencia a esta ruta de acceso en el código como HKEY \_ local \_ Machine \\ REGSTR \_ path \_ CONTROLSFOLDER mediante la \_ macro REGSTR path \_ CONTROLSFOLDER que se define en REGSTR. h.

Las aplicaciones del panel de control que permiten a los controladores de hojas de propiedades reemplazar páginas tienen una subclave en la subclave del panel de control, con el nombre de la aplicación, como el mouse y la presentación. La subclave de la aplicación debe tener una subclave **shellex** con una subclave **PropertySheetHandlers** . Para registrar un controlador de la hoja de propiedades, agregue su GUID a la subclave **PropertySheetHandlers** asociada a la aplicación del panel de control. Para ello, cree una subclave de la subclave **PropertySheetHandlers** , denominada para el controlador de la hoja de propiedades, y establezca su valor predeterminado en el formato de cadena del GUID del controlador.

En el ejemplo siguiente se registra un controlador de la hoja de propiedades para la aplicación del panel de control del mouse por equipo. Para registrarlo por usuario, reemplace **HKEY \_ local \_ Machine** \\ **REGSTR \_ path \_ CONTROLSFOLDER** por **HKEY \_ Current \_ User** \\ **REGSTR \_ rutaDeAcceso \_ CONTROLPANEL**.

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a>Paso 2: implementar un controlador de la hoja de propiedades para una aplicación del panel de control

El procedimiento para implementar un controlador de la hoja de propiedades del panel de control es muy similar al que se describe en [Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md). La principal diferencia es que ahora [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) necesita una implementación que no sea de token en lugar de [**IShellPropSheetExt:: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).

Cuando una aplicación del panel de control está a punto de mostrar su hoja de propiedades, llama una vez al método [**IShellPropSheetExt:: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) del controlador de la hoja de propiedades para cada página que se puede reemplazar. El parámetro *uPageID* se establece en el identificador de la página. Los identificadores de las páginas disponibles se definen en Cplext. h. Los identificadores disponibles actualmente se muestran en la tabla siguiente. 

| Identificador de página                      | Descripción         | Aplicación del panel de control |
|------------------------------|---------------------|---------------------------|
| \_botones del mouse CPLPAGE \_      | La página botones    | Mouse                     |
| CPLPAGE \_ mouse \_ PTRMOTION    | La página de movimiento     | Mouse                     |
| \_rueda del mouse CPLPAGE \_        | La página rueda      | Mouse                     |
| \_velocidad del teclado de CPLPAGE \_     | Página velocidad      | Keyboard                  |
| CPLPAGE \_ Mostrar \_ fondo | Página de fondo | Pantalla                   |



 

## <a name="remarks"></a>Observaciones

El procedimiento para crear y reemplazar una página es idéntico al de agregar una página. Para obtener más información, vea [Cómo registrar e implementar un controlador de hoja de propiedades para un tipo de archivo](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).

 

 



