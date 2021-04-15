---
description: Describe las estructuras utilizadas por las interfaces de vídeo de Microsoft Direct3D 9.
ms.assetid: 584c087e-53f0-42d8-99ed-a0d013379363
title: Estructuras de vídeo de Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ac8e03ff524f7f943c6adbee39b57785112a3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696144"
---
# <a name="direct3d-9-video-structures"></a>Estructuras de vídeo de Direct3D 9

Describe las estructuras utilizadas por las interfaces de vídeo de Microsoft Direct3D 9.



| Estructura                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_OMAC D3D**](d3d-omac.md)<br/> Contiene un código de autentificación de mensajes (MAC) (MAC).<br/>                                                                                                                                                                                                                                                                        |
| [**D3DAES \_ CTR \_ IV**](d3daes-ctr-iv.md)<br/> Contiene un vector de inicialización (IV).<br/>                                                                                                                                                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ configurar \_ entrada**](d3dauthenticatedchannel-configure-input.md)<br/> Contiene datos de entrada para el método [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .<br/>                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ configurar \_ salida**](d3dauthenticatedchannel-configure-output.md)<br/> Contiene la respuesta a una llamada al método [**IDirect3DAuthenticatedChannel9:: configure**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure) .<br/>                                                                                                        |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md)<br/> Contiene los datos de entrada para un comando [**D3DAUTHENTICATEDCONFIGURE \_ Initialize**](d3dauthenticatedconfigure-initialize.md) .<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREPROTECTION**](d3dauthenticatedchannel-configureprotection.md)<br/> Contiene datos de entrada para un comando de [**\_ protección de D3DAUTHENTICATEDCONFIGURE**](d3dauthenticatedconfigure-protection.md) .<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md)<br/> Contiene datos de entrada para un comando [**D3DAUTHENTICATEDCONFIGURE \_ CRYPTOSESSION**](d3dauthenticatedconfigure-cryptosession.md) .<br/>                                                                                                           |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE**](d3dauthenticatedchannel-configuresharedresource.md)<br/> Contiene datos de entrada para un comando [**D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE**](d3dauthenticatedconfigure-sharedresource.md) .<br/>                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION**](d3dauthenticatedchannel-configureuncompressedencryption.md)<br/> Contiene datos de entrada para un comando [**D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedconfigure-encryptionwhenaccessible.md) .<br/>                                                                   |
| [**\_Marcas de protección de D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-protection-flags.md)<br/> Especifica el nivel de protección del contenido de vídeo.<br/>                                                                                                                                                                                                   |
| [**\_Entrada de consulta de D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-input.md)<br/> Contiene datos de entrada para el método [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .<br/>                                                                                                                                     |
| [**Resultado de la \_ consulta D3DAUTHENTICATEDCHANNEL \_**](d3dauthenticatedchannel-query-output.md)<br/> Contiene la respuesta a una llamada al método [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .<br/>                                                                                                                        |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYCHANNELTYPE \_**](d3dauthenticatedchannel-querychanneltype-output.md)<br/> Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md) .<br/>                                                                                                                     |
| [**\_Entrada QUERYCRYPTOSESSION \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-querycryptosession-input.md)<br/> Contiene datos de entrada para una consulta de [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .<br/>                                                                                                                |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_**](d3dauthenticatedchannel-querycryptosession-output.md)<br/> Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md) .<br/>                                                                                                             |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_**](d3dauthenticatedchannel-querydevicehandle-output.md)<br/> Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md) .<br/>                                                                                                                 |
| [**\_Entrada QUERYEVICTIONENCRYPTIONGUID \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)<br/> Contiene datos de entrada para una consulta de [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .<br/>                                                                |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md)<br/> Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md) .<br/>                                                             |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUIDCOUNT \_**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md)<br/> Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md) .<br/>                                         |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_**](d3dauthenticatedchannel-queryinfobustype-output.md)<br/> Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) .<br/>                                                                                             |
| [**\_Entrada QUERYOUTPUTID \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryoutputid-input.md)<br/> Contiene los datos de Intput para una consulta [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .<br/>                                                                                                                                   |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_**](d3dauthenticatedchannel-queryoutputid-output.md)<br/> Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md) .<br/>                                                                                                                                 |
| [**\_Entrada QUERYOUTPUTIDCOUNT \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryoutputidcount-input.md)<br/> Contiene datos de entrada para una consulta de [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .<br/>                                                                                                                |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_**](d3dauthenticatedchannel-queryoutputidcount-output.md)<br/> Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md) .<br/>                                                                                                             |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_**](d3dauthenticatedchannel-queryprotection-output.md)<br/> Contiene la respuesta a una consulta de [**\_ protección de D3DAUTHENTICATEDQUERY**](d3dauthenticatedquery-protection.md) .<br/>                                                                                                                         |
| [**\_Entrada QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ D3DAUTHENTICATEDCHANNEL**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)<br/> Contiene datos de entrada para una consulta de [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .<br/>                                        |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md)<br/> Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) .<br/>                                     |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md)<br/> Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md) .<br/>                 |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md)<br/> Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md) .<br/>                                             |
| [**Salida de D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md)<br/> Contiene la respuesta a una consulta de [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) .<br/> |
| [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps)<br/> Describe las capacidades de protección de contenido de un controlador de pantalla.<br/>                                                                                                                                                                                                                    |
| [**\_Información de bloque de D3DENCRYPTED \_**](d3dencrypted-block-info.md)<br/> Especifica qué bytes se cifran en una superficie de vídeo protegida.<br/>                                                                                                                                                                                                                     |
| [**D3DOVERLAYCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3doverlaycaps)<br/> Especifica las capacidades de superposición de hardware para un dispositivo Direct3D.<br/>                                                                                                                                                                                                                                            |
| [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)<br/> Especifica un búfer para el método [**IDirect3DDXVADevice9:: Execute**](idirect3ddxvadevice9-execute.md) .<br/>                                                                                                                                                                                                  |
| [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo)<br/> Especifica los requisitos para las superficies comprimidas para la aceleración de vídeo de DirectX (DXVA).<br/>                                                                                                                                                                                                         |
| [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)<br/> Especifica las dimensiones y el formato de píxel de las superficies sin comprimir de la descodificación de vídeo de DXVA.<br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 




