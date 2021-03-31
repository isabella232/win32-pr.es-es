---
description: Las siguientes constantes forman el conjunto de comandos válidos de dispositivo de hardware de adquisición de imágenes de Windows (WIA).
ms.assetid: f86a0944-2f2a-467e-a9e8-4cdecfc50175
title: Comandos de dispositivo WIA (Wiadef. h)
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
ms.openlocfilehash: 6e9e732520a256519ebcb21da84eac7ca8d8b630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907999"
---
# <a name="wia-device-commands"></a>Comandos de dispositivo WIA

Las siguientes constantes forman el conjunto de comandos válidos de dispositivo de hardware de adquisición de imágenes de Windows (WIA).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_SYNCHRONIZE"></span><span id="wia_cmd_synchronize"></span><dl> <dt><strong>WIA_CMD_SYNCHRONIZE</strong></dt> </dl></td>
<td style="text-align: left;">Hace que el minicontrolador del dispositivo sincronice los elementos almacenados en caché con el dispositivo de hardware. Si el dispositivo admite el método <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem"><strong>IWiaItem:: AnalyzeItem</strong></a> , la emisión de este comando hace que el minicontrolador descarte los resultados del análisis y restablezca el estado inicial del elemento. Todos los controladores deben ser compatibles con este comando.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_TAKE_PICTURE"></span><span id="wia_cmd_take_picture"></span><dl> <dt><strong>WIA_CMD_TAKE_PICTURE</strong></dt> </dl></td>
<td style="text-align: left;">Hace que un dispositivo WIA adquiera una imagen.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_DELETE_ALL_ITEMS"></span><span id="wia_cmd_delete_all_items"></span><dl> <dt><strong>WIA_CMD_DELETE_ALL_ITEMS</strong></dt> </dl></td>
<td style="text-align: left;">Indica al dispositivo que elimine todos los elementos que se pueden eliminar del árbol de objetos <a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem"><strong>IWiaItem</strong></a> que representan el dispositivo. La eliminación de elementos se evita estableciendo las propiedades del elemento. Para obtener más información, vea <a href="/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-setpropertystream"><strong>IWiaPropertyStorage:: SetPropertyStream</strong></a> y <a href="-wia-property-attributes.md">atributos de propiedad</a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_CHANGE_DOCUMENT"></span><span id="wia_cmd_change_document"></span><dl> <dt><strong>WIA_CMD_CHANGE_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Se utiliza para los escáneres de documentos. Hace que el analizador cargue la siguiente página en su controlador de documentos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_UNLOAD_DOCUMENT"></span><span id="wia_cmd_unload_document"></span><dl> <dt><strong>WIA_CMD_UNLOAD_DOCUMENT</strong></dt> </dl></td>
<td style="text-align: left;">Se utiliza para los escáneres de documentos. Indica al dispositivo que descargue todas las páginas restantes en su controlador de documentos. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_START_FEEDER"></span><span id="wia_cmd_start_feeder"></span><dl> <dt><strong>WIA_CMD_START_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Se usa para los escáneres de documentos que tienen un alimentador de páginas. Indica al dispositivo que inicie el motor del alimentador. Esta característica está disponible a partir de Windows 8.<br/>
<blockquote>
[!Note]<br />
El minicontrolador WIA debe rechazar este comando y devolver <strong>WIA_ERROR_INVALID_COMMAND</strong> cuando no se admite la propiedad <a href="/windows-hardware/drivers/image/wia-ips-feeder-control"><strong>WIA_IPS_FEEDER_CONTROL</strong></a> o se establece en WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_CMD_STOP_FEEDER"></span><span id="wia_cmd_stop_feeder"></span><dl> <dt><strong>WIA_CMD_STOP_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Se usa para los escáneres de documentos que tienen un alimentador de páginas. Indica al dispositivo que detenga el motor del alimentador. Esta característica está disponible a partir de Windows 8.<br/>
<blockquote>
[!Note]<br />
El minicontrolador WIA debe rechazar este comando y devolver <strong>WIA_ERROR_INVALID_COMMAND</strong> cuando no se admite la propiedad <strong>WIA_IPS_FEEDER_CONTROL</strong> o se establece en WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_CMD_PAUSE_FEEDER"></span><span id="wia_cmd_pause_feeder"></span><dl> <dt><strong>WIA_CMD_PAUSE_FEEDER</strong></dt> </dl></td>
<td style="text-align: left;">Se usa para los escáneres de documentos que tienen un alimentador de páginas. Indica al dispositivo que PAUSE el motor del alimentador. Esta característica está disponible a partir de Windows 8.<br/>
<blockquote>
[!Note]<br />
El minicontrolador WIA debe rechazar este comando y devolver <strong>WIA_ERROR_INVALID_COMMAND</strong> cuando no se admite la propiedad <strong>WIA_IPS_FEEDER_CONTROL</strong> o se establece en WIA_FEEDER_CONTROL_AUTO.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
