---
description: Las siguientes constantes especifican el tipo de Windows adquisición de imágenes (WIA).
ms.assetid: 7961f692-088a-4f3b-84e9-5fabb0373c3c
title: Marcas de tipo de elemento de WIA (Wiadef.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WiaItemTypeAnalyze
- WiaItemTypeAudio
- WiaItemTypeBurst
- WiaItemTypeDeleted
- WiaItemTypeDevice
- WiaItemTypeDisconnected
- WiaItemTypeDocument
- WiaItemTypeFile
- WiaItemTypeFolder
- WiaItemTypeFree
- WiaItemTypeGenerated
- WiaItemTypeHasAttachments
- WiaItemTypeHPanorama
- WiaItemTypeImage
- WiaItemTypeProgrammableDataSource
- WiaItemTypeRemoved
- WiaItemTypeRoot
- WiaItemTypeStorage
- WiaItemTypeTransfer
- WiaItemTypeTwainCapabilityPassThrough
- WiaItemTypeVideo
- WiaItemTypeVPanorama
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 5a1a76792a79321ba909607ec7f514a40dac4da92fbbfc4623f87eb99881aaa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965534"
---
# <a name="wia-item-type-flags"></a>Marcas de tipo de elemento WIA

Las siguientes constantes especifican el tipo de Windows adquisición de imágenes (WIA).



| Constante                                                                                                                                                                                                                                                                                     | Descripción                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WiaItemTypeAnalyze"></span><span id="wiaitemtypeanalyze"></span><span id="WIAITEMTYPEANALYZE"></span><dl> <dt>**WiaItemTypeAnalyze**</dt> </dl>                                                                             | Este elemento admite el [**método IWiaItem::AnalyzeItem.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-analyzeitem) *Esta constante no es compatible con Windows* Vista y versiones *posteriores.*<br/>                                                                                                                               |
| <span id="WiaItemTypeAudio"></span><span id="wiaitemtypeaudio"></span><span id="WIAITEMTYPEAUDIO"></span><dl> <dt>**WiaItemTypeAudio**</dt> </dl>                                                                                     | El elemento es un archivo de audio. Solo es válido para los elementos que también tienen el **atributo WiaItemTypeFile.** <br/>                                                                                                                                                                                     |
| <span id="WiaItemTypeBurst"></span><span id="wiaitemtypeburst"></span><span id="WIAITEMTYPEBURST"></span><dl> <dt>**WiaItemTypeBurst**</dt> </dl>                                                                                     | Solo para carpetas. Las imágenes de esta carpeta se tomaron en una secuencia de tiempo continua. *Esta constante no es compatible con Windows* Vista y versiones *posteriores.*<br/>                                                                                                                                       |
| <span id="WiaItemTypeDeleted"></span><span id="wiaitemtypedeleted"></span><span id="WIAITEMTYPEDELETED"></span><dl> <dt>**WiaItemTypeDeleted**</dt> </dl>                                                                             | El elemento se marca como eliminado del árbol. <br/>                                                                                                                                                                                                                                          |
| <span id="WiaItemTypeDevice"></span><span id="wiaitemtypedevice"></span><span id="WIAITEMTYPEDEVICE"></span><dl> <dt>**WiaItemTypeDevice**</dt> </dl>                                                                                 | El elemento representa un dispositivo conectado. <br/>                                                                                                                                                                                                                                               |
| <span id="WiaItemTypeDisconnected"></span><span id="wiaitemtypedisconnected"></span><span id="WIAITEMTYPEDISCONNECTED"></span><dl> <dt>**WiaItemTypeDisconnected**</dt> </dl>                                                         | El elemento representa un dispositivo desconectado. <br/>                                                                                                                                                                                                                                            |
| <span id="WiaItemTypeDocument"></span><span id="wiaitemtypedocument"></span><span id="WIAITEMTYPEDOCUMENT"></span><dl> <dt>**WiaItemTypeDocument**</dt> </dl>                                                                         | El elemento representa un documento. *Esta constante solo es compatible con Windows* Vista y versiones *posteriores.*<br/>                                                                                                                                                                                        |
| <span id="WiaItemTypeFile"></span><span id="wiaitemtypefile"></span><span id="WIAITEMTYPEFILE"></span><dl> <dt>**WiaItemTypeFile**</dt> </dl>                                                                                         | El elemento es un archivo. <br/>                                                                                                                                                                                                                                                                   |
| <span id="WiaItemTypeFolder"></span><span id="wiaitemtypefolder"></span><span id="WIAITEMTYPEFOLDER"></span><dl> <dt>**WiaItemTypeFolder**</dt> </dl>                                                                                 | El elemento es una carpeta. <br/>                                                                                                                                                                                                                                                                 |
| <span id="WiaItemTypeFree"></span><span id="wiaitemtypefree"></span><span id="WIAITEMTYPEFREE"></span><dl> <dt>**WiaItemTypeFree**</dt> </dl>                                                                                         | El elemento no está inicializado o se ha eliminado. <br/>                                                                                                                                                                                                                                        |
| <span id="WiaItemTypeGenerated"></span><span id="wiaitemtypegenerated"></span><span id="WIAITEMTYPEGENERATED"></span><dl> <dt>**WiaItemTypeGenerated**</dt> </dl>                                                                     | Este elemento lo creó la aplicación o el controlador y no tiene un elemento correspondiente en el árbol de elementos del controlador. <br/>                                                                                                                                                               |
| <span id="WiaItemTypeHasAttachments"></span><span id="wiaitemtypehasattachments"></span><span id="WIAITEMTYPEHASATTACHMENTS"></span><dl> <dt>**WiaItemTypeHasAttachments**</dt> </dl>                                                 | El elemento tiene datos adjuntos de archivo. *Esta constante no es compatible con Windows* Vista y versiones *posteriores.*<br/>                                                                                                                                                                                          |
| <span id="WiaItemTypeHPanorama"></span><span id="wiaitemtypehpanorama"></span><span id="WIAITEMTYPEHPANORAMA"></span><dl> <dt>**WiaItemTypeHPanoram**</dt> </dl>                                                                     | El elemento representa una imagen horizontal. *Esta constante no es compatible con Windows* Vista y versiones *posteriores.*<br/>                                                                                                                                                                       |
| <span id="WiaItemTypeImage"></span><span id="wiaitemtypeimage"></span><span id="WIAITEMTYPEIMAGE"></span><dl> <dt>**WiaItemTypeImage**</dt> </dl>                                                                                     | El elemento es un archivo de imagen. Solo es válido para los elementos que también tienen el **atributo WiaItemTypeFile.** <br/>                                                                                                                                                                                     |
| <span id="WiaItemTypeProgrammableDataSource"></span><span id="wiaitemtypeprogrammabledatasource"></span><span id="WIAITEMTYPEPROGRAMMABLEDATASOURCE"></span><dl> <dt>**WiaItemTypeProgrammableDataSource**</dt> </dl>                 | El elemento representa un origen de datos programable. *Esta constante solo es compatible con Windows* Vista y versiones *posteriores.*<br/>                                                                                                                                                                        |
| <span id="WiaItemTypeRemoved"></span><span id="wiaitemtyperemoved"></span><span id="WIAITEMTYPEREMOVED"></span><dl> <dt>**WiaItemTypeRemoved**</dt> </dl>                                                                             | El elemento se ha quitado del dispositivo. <br/>                                                                                                                                                                                                                                            |
| <span id="WiaItemTypeRoot"></span><span id="wiaitemtyperoot"></span><span id="WIAITEMTYPEROOT"></span><dl> <dt>**WiaItemTypeRoot**</dt> </dl>                                                                                         | Identifica el elemento raíz en el árbol de objetos de elemento del dispositivo. *Esta constante solo es compatible con Windows* Vista y versiones *posteriores.*<br/>                                                                                                                                                         |
| <span id="WiaItemTypeStorage"></span><span id="wiaitemtypestorage"></span><span id="WIAITEMTYPESTORAGE"></span><dl> <dt>**WiaItemTypeStorage**</dt> </dl>                                                                             | El elemento representa un medio de almacenamiento. <br/>                                                                                                                                                                                                                                                 |
| <span id="WiaItemTypeTransfer"></span><span id="wiaitemtypetransfer"></span><span id="WIAITEMTYPETRANSFER"></span><dl> <dt>**WiaItemTypeTransfer**</dt> </dl>                                                                         | El elemento se puede transferir. <br/>                                                                                                                                                                                                                                                          |
| <span id="WiaItemTypeTwainCapabilityPassThrough"></span><span id="wiaitemtypetwaincapabilitypassthrough"></span><span id="WIAITEMTYPETWAINCAPABILITYPASSTHROUGH"></span><dl> <dt>**WiaItemTypeTopenCapabilityPassThrough**</dt> </dl> | Este tipo indica que el dispositivo WIA es capaz de recibir datos de funcionalidad TWAIN de la capa de compatibilidad de TWAIN. Si se establece este tipo, cualquier funcionalidad TJDBC que la capa de compatibilidad de TJDBC no entienda, durante una sesión de TJDBC, se pasará al controlador WIA. <br/> |
| <span id="WiaItemTypeVideo"></span><span id="wiaitemtypevideo"></span><span id="WIAITEMTYPEVIDEO"></span><dl> <dt>**WiaItemTypeVideo**</dt> </dl>                                                                                     | El elemento representa el vídeo de streaming. *Esta constante no es compatible con Windows* Server 2003 *,* Windows Vista o *versiones posteriores.*<br/>                                                                                                                                                      |
| <span id="WiaItemTypeVPanorama"></span><span id="wiaitemtypevpanorama"></span><span id="WIAITEMTYPEVPANORAMA"></span><dl> <dt>**WiaItemTypeVPanoram**</dt> </dl>                                                                     | El elemento representa una imagen vertical. *Esta constante no es compatible con Windows* Vista y versiones *posteriores.*<br/>                                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 




