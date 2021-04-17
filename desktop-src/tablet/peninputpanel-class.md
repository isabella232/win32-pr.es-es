---
description: El objeto PenInputPanel le permite agregar fácilmente entradas manuscritas en contexto a las aplicaciones.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: Clase PenInputPanel (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PenInputPanel
- PenInputPanel.IPenInputPanel
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 0564f758d47e516873b8df5020f3f03a5bcb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697819"
---
# <a name="peninputpanel-class"></a>Clase PenInputPanel

\[En desuso. **PenInputPanel** se ha reemplazado por el [Panel de entrada de texto (TIP)](text-input-panel-reference.md).\]

El objeto **PenInputPanel** le permite agregar fácilmente entradas manuscritas en contexto a las aplicaciones.

El objeto **PenInputPanel** está disponible como un objeto que se puede adjuntar y que permite agregar la funcionalidad del panel de entrada de Tablet PC a los controles existentes. La interfaz de usuario está asignada en gran medida por el idioma de entrada actual. Tiene la opción de elegir el método de entrada predeterminado para el objeto **PenInputPanel** , ya sea escritura a mano o teclado. El usuario final puede cambiar entre los métodos de entrada mediante los botones de la interfaz de usuario.

**PenInputPanel** tiene estos tipos de miembros:

-   [Enumeraciones](#enumerations)
-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="enumerations"></a>Enumeraciones

La clase **PenInputPanel** tiene estas enumeraciones.



| Enumeración                    | Descripción                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [**PanelType**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | Define el tipo de entrada disponible actualmente en el objeto **PenInputPanel** .<br/> |



 

### <a name="events"></a>Events

La clase **PenInputPanel** tiene estos eventos.



| Evento                                                  | Descripción                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**InputFailed**](peninputpanel-inputfailed.md)       | Se produce cuando el foco de entrada cambia antes de que el objeto **PenInputPanel** pudiera insertar la entrada del usuario en el control adjunto.<br/> |
| [**PanelChanged**](peninputpanel-panelchanged.md)     | Se produce cuando cambia el objeto **PenInputPanel** entre diseños.<br/>                                                            |
| [**PanelMoving**](peninputpanel-panelmoving.md)       | Se produce cuando se mueve el objeto **PenInputPanel** .<br/>                                                                          |
| [**VisibleChanged**](peninputpanel-visiblechanged.md) | Se produce cuando el objeto **PenInputPanel** se ha mostrado u oculto.<br/>                                                         |



 

### <a name="interfaces"></a>Interfaces

La clase **PenInputPanel** define estas interfaces.



| Interfaz          | Descripción                                                             |
|:-------------------|:------------------------------------------------------------------------|
| **IPenInputPanel** | Este objeto implementa la interfaz com **IPenInputPanel** .<br/> |



 

### <a name="methods"></a>Métodos

La clase **PenInputPanel** tiene estos métodos.



| Método                                                         | Descripción                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | Envía la tinta recopilada al reconocedor y envía el resultado del reconocimiento.<br/>                                                                                                                      |
| [**EnableTsf**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | Cuando se pasa **true**, el **PenInputPanel** intenta enviar texto al control adjunto a través de Text Services Framework (TSF) y permite el uso de la interfaz de usuario de corrección.<br/>    |
| [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | Establece la posición del objeto **PenInputPanel** en una posición de pantalla estática.<br/>                                                                                                               |
| [**Actualizaciones**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | Actualiza y restaura las propiedades de **PenInputPanel** en función de la configuración del panel de entrada de Tablet PC, coloca automáticamente el panel de entrada del lápiz y establece la interfaz de usuario en el panel predeterminado.<br/> |



 

### <a name="properties"></a>Propiedades

La clase **PenInputPanel** tiene estas propiedades.



| Propiedad                                                                  | Tipo de acceso           | Descripción                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | Lectura/escritura<br/> | Obtiene o establece el identificador de ventana del control al que está asociado el objeto **PenInputPanel** .<br/>                                                                     |
| [**Automostrar**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | Lectura/escritura<br/> | Obtiene o establece un valor booleano que especifica si el objeto **PenInputPanel** aparece cuando el foco se establece usando el lápiz.<br/>                                           |
| [**Disponibles**](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | Solo lectura<br/>  | Obtiene un valor booleano que especifica si el objeto **PenInputPanel** está procesando actualmente la entrada de lápiz.<br/>                                                               |
| [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | Lectura/escritura<br/> | Obtiene o establece el tipo de panel que se está usando actualmente para la entrada dentro del objeto **PenInputPanel** .<br/>                                                                |
| [**DefaultPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | Lectura/escritura<br/> | Obtiene o establece el tipo de panel predeterminado que se usa para la entrada dentro del objeto **PenInputPanel** .<br/>                                                         |
| [**Factoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | Lectura/escritura<br/> | Obtiene o establece el nombre de cadena del Factoid que se usa en el reconocimiento.<br/>                                                                                                    |
| [**Height**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | Solo lectura<br/>  | Obtiene el alto del objeto **PenInputPanel** en coordenadas de cliente.<br/>                                                                                              |
| [**HorizontalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | Lectura/escritura<br/> | Obtiene o establece el desplazamiento entre el borde izquierdo del objeto **PenInputPanel** y el borde izquierdo del control al que está asociado.<br/>                             |
| [**Salido**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | Solo lectura<br/>  | Obtiene la ubicación horizontal, o eje x, del borde izquierdo del objeto **PenInputPanel** , en coordenadas de la pantalla.<br/>                                                   |
| [**Arriba**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | Solo lectura<br/>  | Obtiene la ubicación vertical, o eje y, del borde superior del objeto **PenInputPanel** , en coordenadas de la pantalla.<br/>                                                      |
| [**VerticalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | Lectura/escritura<br/> | Obtiene o establece el desplazamiento entre el borde horizontal más cercano del objeto **PenInputPanel** y el borde horizontal más cercano del control al que está asociado.<br/> |
| [**Visible**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | Lectura/escritura<br/> | Obtiene o establece un valor que indica si el objeto **PenInputPanel** está visible.<br/>                                                                                |
| [**Width**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | Solo lectura<br/>  | Obtiene el ancho del objeto **PenInputPanel** en coordenadas de cliente.<br/>                                                                                               |



 

## <a name="remarks"></a>Observaciones

Se puede crear una instancia de este objeto llamando al método [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msinkaut. h (también requiere Msinkaut \_ i. c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programar el panel de entrada mediante la clase PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
