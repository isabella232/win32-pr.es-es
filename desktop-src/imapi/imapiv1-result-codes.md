---
title: Códigos de resultado IMAPIv1 (Imapierror.h)
description: Los métodos de las interfaces IMAPI devuelven S \_ OK si el método se ha realizado correctamente. De lo contrario, devuelven uno de los siguientes códigos de resultado.
ms.assetid: 0143ad10-9b65-4621-9bed-71dadd38c3fc
topic_type:
- apiref
api_name:
- IMAPI_S_PROPERTIESIGNORED
- IMAPI_S_BUFFER_TO_SMALL
- IMAPI_E_NOTOPENED
- IMAPI_E_NOTINITIALIZED
- IMAPI_E_USERABORT
- IMAPI_E_GENERIC
- IMAPI_E_MEDIUM_NOTPRESENT
- IMAPI_E_MEDIUM_INVALIDTYPE
- IMAPI_E_DEVICE_NOPROPERTIES
- IMAPI_E_DEVICE_NOTACCESSIBLE
- IMAPI_E_DEVICE_NOTPRESENT
- IMAPI_E_DEVICE_INVALIDTYPE
- IMAPI_E_INITIALIZE_WRITE
- IMAPI_E_INITIALIZE_ENDWRITE
- IMAPI_E_FILESYSTEM
- IMAPI_E_FILEACCESS
- IMAPI_E_DISCINFO
- IMAPI_E_TRACKNOTOPEN
- IMAPI_E_TRACKOPEN
- IMAPI_E_DISCFULL
- IMAPI_E_BADJOLIETNAME
- IMAPI_E_INVALIDIMAGE
- IMAPI_E_NOACTIVEFORMAT
- IMAPI_E_NOACTIVERECORDER
- IMAPI_E_WRONGFORMAT
- IMAPI_E_ALREADYOPEN
- IMAPI_E_WRONGDISC
- IMAPI_E_FILEEXISTS
- IMAPI_E_STASHINUSE
- IMAPI_E_DEVICE_STILL_IN_USE
- IMAPI_E_LOSS_OF_STREAMING
- IMAPI_E_COMPRESSEDSTASH
- IMAPI_E_ENCRYPTEDSTASH
- IMAPI_E_NOTENOUGHDISKFORSTASH
- IMAPI_E_REMOVABLESTASH
- IMAPI_E_CANNOT_WRITE_TO_MEDIA
- IMAPI_E_TRACK_NOT_BIG_ENOUGH
api_location:
- Imapierror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8956c3975ebc57d069fd0b03ebae9b2ac4c3b720e216d8c132677afc1a7b3793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611815"
---
# <a name="imapiv1-result-codes"></a>Códigos de resultado IMAPIv1

Los métodos de las interfaces IMAPI devuelven S \_ OK si el método se ha realizado correctamente. De lo contrario, devuelven uno de los siguientes códigos de resultado.



| Constante o valor                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                  |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMAPI_S_PROPERTIESIGNORED"></span><span id="imapi_s_propertiesignored"></span><dl> <dt>**IMAPI \_ PROPIEDADES \_ DE SIGNORED**</dt> <dt>0x40200</dt> </dl>                   | Se pasó una propiedad desconocida en un conjunto de propiedades y se omitió.<br/>                                                                                                                                                                              |
| <span id="IMAPI_S_BUFFER_TO_SMALL"></span><span id="imapi_s_buffer_to_small"></span><dl> <dt>**IMAPI \_ S \_ BUFFER \_ TO \_ SMALL**</dt> <dt>0x40201</dt> </dl>                       | El búfer de salida es demasiado pequeño.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTOPENED"></span><span id="imapi_e_notopened"></span><dl> <dt>**IMAPI \_ E \_ NOTOPENED**</dt> <dt>0x8004020b</dt> </dl>                                        | No se ha realizado una llamada a [**IDiscMaster::Open.**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open)<br/>                                                                                                                                                                        |
| <span id="IMAPI_E_NOTINITIALIZED"></span><span id="imapi_e_notinitialized"></span><dl> <dt>**IMAPI \_ E \_ NOTINITIALIZED**</dt> <dt>0x8004020c</dt> </dl>                         | No se ha inicializado un objeto de grabadora.<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_USERABORT"></span><span id="imapi_e_userabort"></span><dl> <dt>**IMAPI \_ E \_ USERABORT**</dt> <dt>0x8004020d</dt> </dl>                                        | El usuario canceló la operación.<br/>                                                                                                                                                                                                                  |
| <span id="IMAPI_E_GENERIC"></span><span id="imapi_e_generic"></span><dl> <dt>**IMAPI \_ E \_ GENERIC**</dt> <dt>0x8004020e</dt> </dl>                                              | Error genérico.<br/>                                                                                                                                                                                                                         |
| <span id="IMAPI_E_MEDIUM_NOTPRESENT"></span><span id="imapi_e_medium_notpresent"></span><dl> <dt>**IMAPI \_ E \_ MEDIUM \_ NOTPRESENT**</dt> <dt>0x8004020f</dt> </dl>               | No hay ningún disco en el dispositivo.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_MEDIUM_INVALIDTYPE"></span><span id="imapi_e_medium_invalidtype"></span><dl> <dt>**IMAPI \_ E \_ MEDIUM \_ INVALIDTYPE**</dt> <dt>0x80040210</dt> </dl>            | El medio no es un tipo que se pueda usar.<br/>                                                                                                                                                                                                         |
| <span id="IMAPI_E_DEVICE_NOPROPERTIES"></span><span id="imapi_e_device_noproperties"></span><dl> <dt>**IMAPI \_ E \_ DEVICE \_ NOPROPERTIES**</dt> <dt>0x80040211</dt> </dl>         | La grabadora no admite ninguna propiedad.<br/>                                                                                                                                                                                                     |
| <span id="IMAPI_E_DEVICE_NOTACCESSIBLE"></span><span id="imapi_e_device_notaccessible"></span><dl> <dt>**IMAPI \_ E \_ DEVICE \_ NOTACCESSIBLE**</dt> <dt>0x80040212</dt> </dl>      | El dispositivo no se puede usar o ya está en uso.<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DEVICE_NOTPRESENT"></span><span id="imapi_e_device_notpresent"></span><dl> <dt>**IMAPI \_ E \_ DEVICE \_ NOTPRESENT**</dt> <dt>0x80040213</dt> </dl>               | El dispositivo no está presente o se ha quitado.<br/>                                                                                                                                                                                                    |
| <span id="IMAPI_E_DEVICE_INVALIDTYPE"></span><span id="imapi_e_device_invalidtype"></span><dl> <dt>**IMAPI \_ E \_ DEVICE \_ INVALIDTYPE**</dt> <dt>0x80040214</dt> </dl>            | La grabadora no admite una operación.<br/>                                                                                                                                                                                                       |
| <span id="IMAPI_E_INITIALIZE_WRITE"></span><span id="imapi_e_initialize_write"></span><dl> <dt>**IMAPI \_ E \_ INITIALIZE \_ WRITE**</dt> <dt>0x80040215</dt> </dl>                  | No se pudo inicializar la interfaz de unidad para escribir.<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_INITIALIZE_ENDWRITE"></span><span id="imapi_e_initialize_endwrite"></span><dl> <dt>**IMAPI \_ E \_ INITIALIZE \_ ENDWRITE**</dt> <dt>0x80040216</dt> </dl>         | No se pudo inicializar la interfaz de unidad para el cierre.<br/>                                                                                                                                                                                         |
| <span id="IMAPI_E_FILESYSTEM"></span><span id="imapi_e_filesystem"></span><dl> <dt>**IMAPI \_ E \_ FILESYSTEM**</dt> <dt>0x80040217</dt> </dl>                                     | Error al habilitar o deshabilitar el acceso al sistema de archivos o durante la detección de inserción automática.<br/>                                                                                                                                                 |
| <span id="IMAPI_E_FILEACCESS"></span><span id="imapi_e_fileaccess"></span><dl> <dt>**IMAPI \_ E \_ FILEACCESS**</dt> <dt>0x80040218</dt> </dl>                                     | Error al escribir el archivo de imagen.<br/>                                                                                                                                                                                                   |
| <span id="IMAPI_E_DISCINFO"></span><span id="imapi_e_discinfo"></span><dl> <dt>**IMAPI \_ E \_ DISCINFO**</dt> <dt>0x80040219</dt> </dl>                                           | Se produjo un error al intentar leer datos de disco del dispositivo.<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_TRACKNOTOPEN"></span><span id="imapi_e_tracknotopen"></span><dl> <dt>**IMAPI \_ E \_ TRACKNOTOPEN**</dt> <dt>0x8004021a</dt> </dl>                               | Una pista de audio no está abierta para escritura.<br/>                                                                                                                                                                                                           |
| <span id="IMAPI_E_TRACKOPEN"></span><span id="imapi_e_trackopen"></span><dl> <dt>**IMAPI \_ E \_ TRACKOPEN**</dt> <dt>0x8004021b</dt> </dl>                                        | Ya se está staged una pista de audio abierta.<br/>                                                                                                                                                                                                      |
| <span id="IMAPI_E_DISCFULL"></span><span id="imapi_e_discfull"></span><dl> <dt>**IMAPI \_ E \_ DISCFULL**</dt> <dt>0x8004021c</dt> </dl>                                           | El disco no puede contener más datos.<br/>                                                                                                                                                                                                               |
| <span id="IMAPI_E_BADJOLIETNAME"></span><span id="imapi_e_badjolietname"></span><dl> <dt>**IMAPI \_ E \_ BADJOLIETNAME**</dt> <dt>0x8004021d</dt> </dl>                            | La aplicación intentó agregar un elemento con nombre no correcta a un disco.<br/>                                                                                                                                                                                     |
| <span id="IMAPI_E_INVALIDIMAGE"></span><span id="imapi_e_invalidimage"></span><dl> <dt>**IMAPI \_ E \_ INVALIDIMAGE**</dt> <dt>0x8004021e</dt> </dl>                               | La imagen con fases no es adecuada para una grabación. Se ha dañado o borrado y no tiene contenido utilizable.<br/>                                                                                                                                          |
| <span id="IMAPI_E_NOACTIVEFORMAT"></span><span id="imapi_e_noactiveformat"></span><dl> <dt>**IMAPI \_ E \_ NOACTIVEFORMAT**</dt> <dt>0x8004021f</dt> </dl>                         | No se ha seleccionado un maestro de formato activo [**mediante IDiscMaster::SetActiveDiscMasterFormat**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscmasterformat).<br/>                                                                                                      |
| <span id="IMAPI_E_NOACTIVERECORDER"></span><span id="imapi_e_noactiverecorder"></span><dl> <dt>**IMAPI \_ E \_ NOACTIVERECORDER**</dt> <dt>0x80040220</dt> </dl>                   | No se ha seleccionado una grabadora de discos activa con [**IDiscMaster::SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder).<br/>                                                                                                              |
| <span id="IMAPI_E_WRONGFORMAT"></span><span id="imapi_e_wrongformat"></span><dl> <dt>**IMAPI \_ E \_ WRONGFORMAT**</dt> <dt>0x80040221</dt> </dl>                                  | Se ha realizado una llamada a [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) cuando [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster) es el formato activo o viceversa. Para usar un formato diferente, cambie el formato y borre el contenido del archivo de imagen.<br/> |
| <span id="IMAPI_E_ALREADYOPEN"></span><span id="imapi_e_alreadyopen"></span><dl> <dt>**IMAPI \_ E \_ ALREADYOPEN**</dt> <dt>0x80040222</dt> </dl>                                  | La aplicación ya ha realizado una llamada a [**IDiscMaster::Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open) en este objeto.<br/>                                                                                                                            |
| <span id="IMAPI_E_WRONGDISC"></span><span id="imapi_e_wrongdisc"></span><dl> <dt>**IMAPI \_ E \_ WRONGDISC**</dt> <dt>0x80040223</dt> </dl>                                        | El disco de sesión múltiple imapi se ha quitado de la grabadora activa.<br/>                                                                                                                                                                           |
| <span id="IMAPI_E_FILEEXISTS"></span><span id="imapi_e_fileexists"></span><dl> <dt>**IMAPI \_ E \_ FILEEXISTS**</dt> <dt>0x80040224</dt> </dl>                                     | El archivo que se va a agregar ya está en el archivo de imagen y no se ha establecido la marca de sobrescritura.<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_STASHINUSE"></span><span id="imapi_e_stashinuse"></span><dl> <dt>**IMAPI \_ E \_ STAASHIUSE**</dt> <dt>0x80040225</dt> </dl>                                     | Otra aplicación ya usa el archivo de stash IMAPI necesario para la fase de una imagen de disco. Vuelva a intentarlo más tarde.<br/>                                                                                                                                        |
| <span id="IMAPI_E_DEVICE_STILL_IN_USE"></span><span id="imapi_e_device_still_in_use"></span><dl> <dt>**IMAPI \_ E \_ DEVICE STILL IN \_ \_ \_ USE**</dt> <dt>0x80040226</dt> </dl>       | Otra aplicación ya usa este dispositivo, por lo que IMAPI no puede acceder al dispositivo.<br/>                                                                                                                                                              |
| <span id="IMAPI_E_LOSS_OF_STREAMING"></span><span id="imapi_e_loss_of_streaming"></span><dl> <dt>**IMAPI \_ E \_ PÉRDIDA DE STREAMING \_ \_ 0x80040227**</dt> <dt></dt> </dl>              | Se perdió el streaming de contenido; es posible que se haya producido un búfer en ejecución.<br/>                                                                                                                                                                                 |
| <span id="IMAPI_E_COMPRESSEDSTASH"></span><span id="imapi_e_compressedstash"></span><dl> <dt>**IMAPI \_ E \_ COMPRESSEDSTASH**</dt> <dt>0x80040228</dt> </dl>                      | El almacenamiento stash se encuentra en un volumen comprimido y no se puede leer.<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_ENCRYPTEDSTASH"></span><span id="imapi_e_encryptedstash"></span><dl> <dt>**IMAPI \_ E \_ ENCRYPTEDSTASH**</dt> <dt>0x80040229</dt> </dl>                         | El almacenamiento stash se encuentra en un volumen cifrado y no se puede leer.<br/>                                                                                                                                                                                   |
| <span id="IMAPI_E_NOTENOUGHDISKFORSTASH"></span><span id="imapi_e_notenoughdiskforstash"></span><dl> <dt>**IMAPI \_ E \_ NOTENDISKFORSTASH**</dt> <dt>0x8004022a</dt> </dl>    | No hay suficiente espacio libre para crear el archivo de almacenamiento stash en el volumen especificado.<br/>                                                                                                                                                                  |
| <span id="IMAPI_E_REMOVABLESTASH"></span><span id="imapi_e_removablestash"></span><dl> <dt>**IMAPI \_ E \_ REMOVABLESTASH**</dt> <dt>0x8004022b</dt> </dl>                         | La ubicación de almacenamiento stash seleccionada se encuentra en un medio extraíble.<br/>                                                                                                                                                                                              |
| <span id="IMAPI_E_CANNOT_WRITE_TO_MEDIA"></span><span id="imapi_e_cannot_write_to_media"></span><dl> <dt>**IMAPI \_ E \_ NO SE PUEDE ESCRIBIR EN \_ \_ \_ ARCHIVOS**</dt> <dt>0X8004022C</dt> </dl> | No se puede escribir en el medio.<br/>                                                                                                                                                                                                                   |
| <span id="IMAPI_E_TRACK_NOT_BIG_ENOUGH"></span><span id="imapi_e_track_not_big_enough"></span><dl> <dt>**IMAPI \_ E \_ TRACK NOT BIG \_ \_ \_ ENOUGH**</dt> <dt>0x8004022d</dt> </dl>    | La pista no es lo suficientemente grande.<br/>                                                                                                                                                                                                                      |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Imapierror.h</dt> </dl> |



 

 





