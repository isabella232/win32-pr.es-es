---
description: El objeto PenInputPanel permite agregar fácilmente entradas de lápiz en su lugar a las aplicaciones.
ms.assetid: ad63302e-b386-4b32-95bf-be1129839c33
title: PenInputPanel (clase, Msinputut.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359636"
---
# <a name="peninputpanel-class"></a>PenInputPanel (clase)

\[En desuso. **PenInputPanel se** ha reemplazado por el [Panel de entrada de texto (TIP).](text-input-panel-reference.md)\]

El **objeto PenInputPanel** permite agregar fácilmente entradas de lápiz en su lugar a las aplicaciones.

El **objeto PenInputPanel** está disponible como un objeto adjuntable que permite agregar la funcionalidad panel de entrada de Tablet PC a los controles existentes. La interfaz de usuario se exige en gran medida por el idioma de entrada actual. Tiene la opción de elegir el método de entrada predeterminado para el **objeto PenInputPanel,** ya sea escritura a mano o teclado. El usuario final puede cambiar entre métodos de entrada mediante botones en la interfaz de usuario.

**PenInputPanel tiene** estos tipos de miembros:

-   [Enumeraciones](#enumerations)
-   [Eventos](#events)
-   [Interfaces](#interfaces)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="enumerations"></a>Enumeraciones

La **clase PenInputPanel** tiene estas enumeraciones.



| Enumeración                    | Descripción                                                                               |
|:-------------------------------|:------------------------------------------------------------------------------------------|
| [**PanelType**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) | Define el tipo de entrada disponible actualmente en el **objeto PenInputPanel.**<br/> |



 

### <a name="events"></a>Eventos

La **clase PenInputPanel** tiene estos eventos.



| Evento                                                  | Descripción                                                                                                                             |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**InputFailed**](peninputpanel-inputfailed.md)       | Se produce cuando el foco de entrada cambia antes **de que el objeto PenInputPanel** pueda insertar la entrada del usuario en el control adjunto.<br/> |
| [**PanelChanged**](peninputpanel-panelchanged.md)     | Se produce cuando el **objeto PenInputPanel** cambia entre diseños.<br/>                                                            |
| [**PanelMoving**](peninputpanel-panelmoving.md)       | Se produce cuando se **mueve el objeto PenInputPanel.**<br/>                                                                          |
| [**VisibleChanged**](peninputpanel-visiblechanged.md) | Se produce cuando el **objeto PenInputPanel** se ha mostrado u se ha ocultado.<br/>                                                         |



 

### <a name="interfaces"></a>Interfaces

La **clase PenInputPanel** define estas interfaces.



| Interfaz          | Descripción                                                             |
|:-------------------|:------------------------------------------------------------------------|
| **IPenInputPanel** | Este objeto implementa la interfaz COM **IPenInputPanel.**<br/> |



 

### <a name="methods"></a>Métodos

La **clase PenInputPanel** tiene estos métodos.



| Método                                                         | Descripción                                                                                                                                                                                             |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitPendingInput**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-commitpendinginput) | Envía la entrada de lápiz recopilada al reconocedor y publica el resultado del reconocimiento.<br/>                                                                                                                      |
| [**EnableTsf**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-enabletsf)                   | Cuando se **pasa TRUE**, **PenInputPanel** intenta enviar texto al control adjunto a través de Text Services Framework (TSF) y habilita el uso de la interfaz de usuario de corrección.<br/>    |
| [**Moveto**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)                         | Establece la posición del **objeto PenInputPanel** en una posición de pantalla estática.<br/>                                                                                                               |
| [**Actualizar**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)                       | Actualiza y restaura las propiedades **de PenInputPanel** según la configuración del panel de entrada de Tablet PC, coloca automáticamente el panel de entrada del lápiz y establece la interfaz de usuario en el panel predeterminado.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase PenInputPanel** tiene estas propiedades.



| Propiedad                                                                  | Tipo de acceso           | Descripción                                                                                                                                                                    |
|:--------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachedEditWindow**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_attachededitwindow)<br/> | Lectura y escritura<br/> | Obtiene o establece el identificador de ventana del control al que está asociado el objeto **PenInputPanel.**<br/>                                                                     |
| [**Autoshow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)<br/>                     | Lectura y escritura<br/> | Obtiene o establece un valor booleano que especifica si el **objeto PenInputPanel** aparece cuando el foco se establece mediante el lápiz.<br/>                                           |
| [**Ocupado**](/windows/desktop/api/Peninputpanel/nf-peninputpanel-ipeninputpanel-get_busy)<br/>                             | Solo lectura<br/>  | Obtiene un valor booleano que especifica si el **objeto PenInputPanel** está procesando actualmente la entrada de lápiz.<br/>                                                               |
| [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel)<br/>             | Lectura y escritura<br/> | Obtiene o establece el tipo de panel que se usa actualmente para la entrada dentro del **objeto PenInputPanel.**<br/>                                                                |
| [**DefaultPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_defaultpanel)<br/>             | Lectura y escritura<br/> | Obtiene o establece qué tipo de panel es el tipo de panel predeterminado que se usa para la entrada dentro del **objeto PenInputPanel.**<br/>                                                         |
| [**Factoid**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)<br/>                       | Lectura y escritura<br/> | Obtiene o establece el nombre de cadena del factoid usado en el reconocimiento.<br/>                                                                                                    |
| [**Alto**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_height)<br/>                         | Solo lectura<br/>  | Obtiene el alto del objeto **PenInputPanel** en coordenadas de cliente.<br/>                                                                                              |
| [**HorizontalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_horizontaloffset)<br/>     | Lectura y escritura<br/> | Obtiene o establece el desplazamiento entre el borde izquierdo del **objeto PenInputPanel** y el borde izquierdo del control al que está asociado.<br/>                             |
| [**Left**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_left)<br/>                             | Solo lectura<br/>  | Obtiene la ubicación horizontal o del eje X del borde izquierdo del **objeto PenInputPanel,** en coordenadas de pantalla.<br/>                                                   |
| [**Arriba**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_top)<br/>                               | Solo lectura<br/>  | Obtiene la ubicación vertical o del eje Y del borde superior del **objeto PenInputPanel,** en coordenadas de pantalla.<br/>                                                      |
| [**VerticalOffset**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_verticaloffset)<br/>         | Lectura y escritura<br/> | Obtiene o establece el desplazamiento entre el borde horizontal más cercano del objeto **PenInputPanel** y el borde horizontal más cercano del control al que está asociado.<br/> |
| [**Visible**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_visible)<br/>                       | Lectura y escritura<br/> | Obtiene o establece un valor que indica si el **objeto PenInputPanel** está visible.<br/>                                                                                |
| [**Ancho**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_width)<br/>                           | Solo lectura<br/>  | Obtiene el ancho del objeto **PenInputPanel** en coordenadas de cliente.<br/>                                                                                               |



 

## <a name="remarks"></a>Observaciones

Se puede crear una instancia de este objeto llamando al [**método CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) en C++.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de XP Tablet PC \[ Edition\]<br/>                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                                           |
| Encabezado<br/>                   | <dl> <dt>Msgniut.h (también requiere Ms ashut \_ i.c)</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Programar el panel de entrada mediante la clase PenInputPanel](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
