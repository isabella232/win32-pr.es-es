---
title: Propiedades estándar
description: Propiedades estándar
ms.assetid: 08b7c388-a362-4d71-ac24-93675984881f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ab30dd644231c5c11a9f1e4d7ccf9c861ae2fa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078405"
---
# <a name="standard-properties"></a>Propiedades estándar

OLE define un conjunto de DISPID estándar para los tres tipos de propiedades: control, ambiente y extendido. En las tablas siguientes se enumeran estos estándares para las propiedades de control, las propiedades de ambiente y las propiedades extendidas.



| Propiedad de control                                                                               | Tipo                             | Descripción                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------|----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BackColor, ForeColor, FillColor, BorderColor<br/>                                        | **\_color OLE**<br/>        | Combinación de colores del control<br/>                                                                                                                                                                                                    |
| BackStyle, FillStyle, BorderStyle, BorderWidth, BorderVisible, DrawStyle, DrawWidth<br/> | **corto** o **largo**<br/> | Bits que definen el comportamiento visual de un control, como sólido o transparente, con bordes gruesos o finos, estilos de línea, etc.<br/>                                                                                    |
| Fuente<br/>                                                                                | **IDispatch \***<br/>      | Fuente utilizada en el control, que es un puntero **IDispatch** a un objeto de fuente estándar. Vea el [objeto fuente estándar](standard-font-object.md) para obtener más información.<br/>                                                         |
| Título, texto<br/>                                                                       | **UTILICEN**<br/>              | Cadenas que contienen la etiqueta del control (el título) o su contenido textual (el texto). Tenga en cuenta que el título no tiene necesariamente el nombre del control en el contenedor. Vea la propiedad nombre extendido en la tabla siguiente.<br/> |
| habilitado<br/>                                                                             | **BOOLEANO**<br/>              | Determina si el control está habilitado o deshabilitado. Si está deshabilitado, es probable que el control esté atenuado.<br/>                                                                                                                           |
| Periodo<br/>                                                                              | **IDENTIFICADOR**<br/>              | Identificador de ventana del control, si tiene uno.<br/>                                                                                                                                                                              |
| TabStop<br/>                                                                             | **BOOLEANO**<br/>              | Determina si este control es una tabulación.<br/>                                                                                                                                                                                |



 



| Propiedad Ambient                         | Tipo                        | Descripción                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BackColor, ForeColor<br/>          | **\_color OLE**<br/>   | Proporciona controles con los colores de fondo y de primer plano predeterminados. El uso de un control es opcional.<br/>                                                                                                                                                                                                                                                                                          |
| Fuente<br/>                          | **IDispatch \***<br/> | Un puntero a un objeto de fuente estándar que define la fuente predeterminada del formulario. El uso de un control es opcional. Vea el [objeto fuente estándar](standard-font-object.md) para obtener más información.<br/>                                                                                                                                                                                                    |
| LocaleID<br/>                      | **LCID**<br/>         | Lenguaje utilizado en el contenedor. Se recomienda el uso de un control.<br/>                                                                                                                                                                                                                                                                                                                        |
| En modo usuario<br/>                      | **BOOLEANO**<br/>         | Describe si el contenedor está en modo de diseño (**false**) o en modo de ejecución (**true**), que debe usar un control para cambiar su funcionalidad disponible según sea necesario.<br/>                                                                                                                                                                                                                      |
| UIDead<br/>                        | **BOOLEANO**<br/>         | Describe si el contenedor está en un modo en el que los controles deben omitir los datos proporcionados por el usuario. Esto se aplica independientemente del modo de modo de aplicación. Un contenedor siempre puede establecer UIDead en **true** en el modo de diseño, y puede establecerlo en **true** cuando ha alcanzado un punto de interrupción o como en el modo de ejecución. Un control debe prestar atención a esta propiedad.<br/>                                                                |
| MessageReflect<br/>                | **BOOLEANO**<br/>         | Especifica si el contenedor desea recibir mensajes de Windows como WM \_ CTLCOLOR, WM \_ DRAWITEM, WM \_ PARENTNOTIFY, etc., como eventos.<br/>                                                                                                                                                                                                                                           |
| SupportsMnemonics<br/>             | **BOOLEANO**<br/>         | Describe si el contenedor procesa los códigos de tecla o no. Un control puede hacer todo lo que desee con esta información, como no utilizar caracteres de subrayado, normalmente se usaría como mnemotécnico.<br/>                                                                                                                                                                                                 |
| ShowGrabHandles, ShowHatching<br/> | **BOOLEANO**<br/>         | Describe si un control debe mostrar un borde sombreado o controladores de arrastre (en el borde de sombreado) cuando están activos en contexto. Los controles deben obedecer estas propiedades, lo que permite al contenedor el control final sobre quién dibuja realmente estos bits de la interfaz de usuario. Un contenedor de controles puede querer dibujar su propia en lugar de confiar en cada control, en cuyo caso estos ambiente siempre serán **false**.<br/> |
| DisplayAsDefault<br/>              | **BOOLEANO**<br/>         | El contenedor expondrá un **valor true** para esta propiedad a través de cualquier sitio que contenga lo que está marcado como el botón predeterminado cuando el control de botón debe dibujarse con un marco predeterminado más grueso.<br/>                                                                                                                                                                                         |



 



| Propiedad extendida          | Tipo                        | Descripción                                                           |
|----------------------------|-----------------------------|-----------------------------------------------------------------------|
| Nombre<br/>            | **UTILICEN**<br/>         | Nombre del contenedor del control.<br/>                      |
| Visible<br/>         | **BOOLEANO**<br/>         | Visibilidad del control.<br/>                                  |
| Parent<br/>          | **IDispatch \***<br/> | Dispinterface del formulario que contiene el control.<br/>      |
| Predeterminado, cancelar<br/> | **BOOLEANO**<br/>         | Indica si este control es el botón predeterminado o cancelar.<br/> |



 

Todas estas propiedades estándar tienen valores DISPID negativos, que indican su estado estándar.

Tenga en cuenta que para evitar conflictos en los símbolos de programación para estos DISPID, todas las propiedades de ambiente tienen símbolos en la propiedad de ambiente DISPID del formulario \_ \_  como en el de tipo FORECOLOR de ambiente de DISPID \_ \_ . Todos los demás símbolos usan la \_ *propiedad* DISPID como de costumbre.

Algunas propiedades de ambiente, así como las propiedades de control, implican colores. El tipo de **\_ color OLE** mencionado en las tablas anteriores puede hacer referencia a un tipo **COLORREF** estándar, un índice a una paleta, un índice relativo a la paleta o un índice de color del sistema usado con la función [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) . La función [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor) convierte un tipo **de \_ color OLE** en un tipo **COLORREF** a partir de una paleta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Propiedades del control](control-properties.md)
</dt> </dl>

 

