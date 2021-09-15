---
title: Propiedades estándar
description: Propiedades estándar
ms.assetid: 08b7c388-a362-4d71-ac24-93675984881f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ab30dd644231c5c11a9f1e4d7ccf9c861ae2fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466610"
---
# <a name="standard-properties"></a>Propiedades estándar

OLE define un conjunto de DISPID estándar para los tres tipos de propiedades: control, ambiente y extendido. En las tablas siguientes se muestran estos estándares para propiedades de control, propiedades ambientales y propiedades extendidas.



| Propiedad de control                                                                               | Tipo                             | Descripción                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BackColor, ForeColor, FillColor, BorderColor<br/>                                        | **OLE \_ COLOR**<br/>        | Combinación de colores del control<br/>                                                                                                                                                                                                    |
| BackStyle, FillStyle, BorderStyle, BorderWidth, BorderVisible, DrawStyle, DrawWidth<br/> | **short** o **long**<br/> | Bits que definen el comportamiento visual de un control, como ser sólido o transparente, tener bordes gruesos o finos, estilos de línea, etc.<br/>                                                                                    |
| Fuente<br/>                                                                                | **IDispatch \** _<br/>      | Fuente usada en el control , que es un puntero _ *IDispatch** a un objeto de fuente estándar. Vea [Standard Font Object (Objeto de fuente](standard-font-object.md) estándar) para obtener más información.<br/>                                                         |
| Título, texto<br/>                                                                       | **BSTR**<br/>              | Cadenas que contienen la etiqueta del control (el título) o su contenido textual (el texto). Tenga en cuenta que el título no da necesariamente nombre al control en el contenedor. Vea la propiedad Nombre extendida en la tabla siguiente.<br/> |
| habilitado<br/>                                                                             | **BOOL**<br/>              | Determina si el control está habilitado o deshabilitado. Si está deshabilitado, es probable que el control esté atenuado.<br/>                                                                                                                           |
| Periodo<br/>                                                                              | **HWND**<br/>              | Identificador de ventana del control, si tiene uno.<br/>                                                                                                                                                                              |
| Tabstop<br/>                                                                             | **BOOL**<br/>              | Determina si este control es un tabulador.<br/>                                                                                                                                                                                |



 



| Propiedad Ambient                         | Tipo                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BackColor, ForeColor<br/>          | **OLE \_ COLOR**<br/>   | Proporciona controles con los colores de fondo y primer plano predeterminados. El uso por parte de un control es opcional.<br/>                                                                                                                                                                                                                                                                                          |
| Fuente<br/>                          | **Idispatch \***<br/> | Puntero a un objeto de fuente estándar que define la fuente predeterminada para el formulario. El uso por parte de un control es opcional. Vea [Standard Font Object (Objeto de fuente](standard-font-object.md) estándar) para obtener más información.<br/>                                                                                                                                                                                                    |
| LocaleID<br/>                      | **LCID**<br/>         | Idioma utilizado en el contenedor. Se recomienda su uso por parte de un control .<br/>                                                                                                                                                                                                                                                                                                                        |
| UserMode<br/>                      | **BOOL**<br/>         | Describe si el contenedor está en modo de diseño **(FALSE)** o en modo de ejecución **(TRUE),** que un control debe usar para cambiar su funcionalidad disponible según sea necesario.<br/>                                                                                                                                                                                                                      |
| UIDead<br/>                        | **BOOL**<br/>         | Describe si el contenedor está en un modo en el que los controles deben omitir la entrada del usuario. Esto se aplica independientemente de UserMode. Un contenedor siempre puede establecer UIDead en **TRUE** en modo de diseño y puede establecerlo en **TRUE** cuando se ha alcanzado un punto de interrupción o tal durante el modo de ejecución. Un control debe prestar atención a esta propiedad.<br/>                                                                |
| MessageReflect<br/>                | **BOOL**<br/>         | Especifica si el contenedor desea recibir mensajes Windows como WM \_ CTLCOLOR, WM \_ DRAWITEM, WM PARENTNOTIFY, y así sucesivamente como \_ eventos.<br/>                                                                                                                                                                                                                                           |
| SupportsMnemonics<br/>             | **BOOL**<br/>         | Describe si el contenedor procesa mnemonics o no. Un control puede hacer lo que quiera con esta información, como no subraya los caracteres que normalmente usaría como mnemotécnico.<br/>                                                                                                                                                                                                 |
| ShowGrabHandles, ShowHatching<br/> | **BOOL**<br/>         | Describe si un control debe mostrar un borde de sombreado o controladores de agarre (en el borde de sombreado) cuando está activo en su lugar. Los controles deben cumplir estas propiedades, lo que da al contenedor el control final sobre quién dibuja realmente estos bits de la interfaz de usuario. Es posible que un contenedor de controles quiera dibujar su propio en lugar de confiar en cada control, en cuyo caso estos ambientes siempre serán **FALSE.**<br/> |
| DisplayAsDefault<br/>              | **BOOL**<br/>         | El contenedor expondrá un **valor TRUE** para esta propiedad a través de cualquier sitio que contenga lo que se marca como botón predeterminado cuando el control de botón debe dibujarse con un marco predeterminado más grueso.<br/>                                                                                                                                                                                         |



 



| Propiedad extendida          | Tipo                        | Descripción                                                           |
|----------------------------|-----------------------------|-----------------------------------------------------------------------|
| Nombre<br/>            | **BSTR**<br/>         | Nombre del contenedor para el control.<br/>                      |
| Visible<br/>         | **BOOL**<br/>         | Visibilidad del control.<br/>                                  |
| Parent<br/>          | **Idispatch \***<br/> | Interfaz dispinterface del formulario que contiene el control.<br/>      |
| Valor predeterminado, Cancelar<br/> | **BOOL**<br/>         | Indica si este control es el botón predeterminado o cancelar.<br/> |



 

Todas estas propiedades estándar tienen valores DISPID negativos, lo que indica su estado estándar.

Tenga en cuenta que para evitar conflictos en los símbolos de programación para estos DISPID, todas las propiedades ambientales reciben símbolos con la forma PROPIEDAD DISPID AMBIENT como en \_ \_  DISPID \_ AMBIENT \_ FORECOLOR. Todos los demás símbolos usan la propiedad DISPID \_  como de costumbre.

Algunas propiedades ambientales, así como las propiedades de control, implican colores. El tipo **\_ DE COLOR OLE** mencionado en las tablas anteriores puede hacer referencia a un tipo **COLORREF** estándar, un índice a una paleta, un índice relativo a la paleta o un índice de color del sistema utilizado con la [**función GetSysColor.**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) La [**función OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor) convierte un tipo **OLE \_ COLOR** en un **tipo COLORREF** dada una paleta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control](control-properties.md)
</dt> </dl>

 

