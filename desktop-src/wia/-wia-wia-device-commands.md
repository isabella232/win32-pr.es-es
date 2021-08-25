---
description: Las siguientes constantes forman el conjunto de comandos de dispositivo de hardware Windows adquisición de imágenes (WIA) válidos.
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: Comandos de dispositivo WIA (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_CMD_SYNCHRONIZE
- WIA_CMD_TAKE_PICTURE
- WIA_CMD_DELETE_ALL_ITEMS
- WIA_CMD_CHANGE_DOCUMENT
- WIA_CMD_UNLOAD_DOCUMENT
- WIA_CMD_START_FEEDER
- WIA_CMD_STOP_FEEDER
- WIA_CMD_PAUSE_FEEDER
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 08aeb26502686d2550d872bcfa845e3c68230ac4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467112"
---
# <a name="wia-device-commands"></a>Comandos de dispositivo WIA

Las siguientes constantes forman el conjunto de comandos de dispositivo de hardware Windows adquisición de imágenes (WIA) válidos.




| Constante | Descripción | 
|----------|-------------|
| <span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl><dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt></dl> | Hace que el minidriver del dispositivo sincronice los elementos almacenados en caché con el dispositivo de hardware. Si el dispositivo admite el método <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem::AnalyzeItem,</strong></a> la emisión de este comando hace que el minidriver descarte los resultados del análisis y restablezca el elemento a su estado inicial. Todos los controladores deben admitir este comando.<br /> | 
| <span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl><dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt></dl> | Hace que un dispositivo WIA adquiera una imagen.<br /> | 
| <span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl><dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt></dl> | Indica al dispositivo que elimine todos los elementos que se pueden eliminar del árbol de <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>objetos IWiaItem</strong></a> que representan el dispositivo. La eliminación de elementos se impide estableciendo las propiedades del elemento. Para obtener más información, <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>vea IWiaPropertyStorage::SetPropertyStream</strong></a> y <a href="-wia-property-attributes.md">Property Attributes</a>.<br /> | 
| <span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl><dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt></dl> | Se usa para escáneres de documentos. Hace que el analizador cargue la página siguiente en su controlador de documentos.<br /> | 
| <span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl><dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt></dl> | Se usa para escáneres de documentos. Indica al dispositivo que descargue todas las páginas restantes en su controlador de documentos. <br /> | 
| <span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl><dt><strong>WIA_CMD_START_FEEDER</strong></dt></dl> | Se usa para escáneres de documentos que tienen un avance de página. Indica al dispositivo que inicie el motor del feeder. Esta característica está disponible a partir de Windows 8.<br /><blockquote>[!Note]<br />El minidriver wia debe rechazar <strong></strong> este comando y devolver WIA_ERROR_INVALID_COMMAND cuando no se admite la propiedad <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> o se establece en WIA_FEEDER_CONTROL_AUTO.</blockquote><br /> | 
| <span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl><dt><strong>WIA_CMD_STOP_FEEDER</strong></dt></dl> | Se usa para escáneres de documentos que tienen un avance de página. Indica al dispositivo que detenga el motor del feeder. Esta característica está disponible a partir de Windows 8.<br /><blockquote>[!Note]<br />El minidriver wia debe rechazar <strong></strong> este comando y devolver WIA_ERROR_INVALID_COMMAND cuando no se admite la propiedad <strong>WIA_IPS_FEEDER_CONTROL</strong> o se establece en WIA_FEEDER_CONTROL_AUTO.</blockquote><br /> | 
| <span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl><dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt></dl> | Se usa para escáneres de documentos que tienen un avance de página. Indica al dispositivo que pause el motor del feeder. Esta característica está disponible a partir de Windows 8.<br /><blockquote>[!Note]<br />El minidriver wia debe rechazar <strong></strong> este comando y devolver WIA_ERROR_INVALID_COMMAND cuando no se admite la propiedad <strong>WIA_IPS_FEEDER_CONTROL</strong> o se establece en WIA_FEEDER_CONTROL_AUTO.</blockquote><br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones de \[ escritorio XP\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
