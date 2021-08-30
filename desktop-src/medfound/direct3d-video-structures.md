---
description: Describe las estructuras usadas por las interfaces de vídeo de Microsoft Direct3D 9.
ms.assetid: 584c087e-53f0-42d8-99ed-a0d013379363
title: Estructuras de vídeo de Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c4093ccc5b629441728f89d230276722527dbdb6ea80d8d77465a37ca14ca7e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942635"
---
# <a name="direct3d-9-video-structures"></a>Estructuras de vídeo de Direct3D 9

Describe las estructuras usadas por las interfaces de vídeo de Microsoft Direct3D 9.



| Estructura                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D \_ OMAC**](d3d-omac.md)<br/> Contiene un código de autenticación de mensajes (MAC).<br/>                                                                                                                                                                                                                                                                        |
| [**D3DAES \_ CTR \_ IV**](d3daes-ctr-iv.md)<br/> Contiene un vector de inicialización (IV).<br/>                                                                                                                                                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ INPUT**](d3dauthenticatedchannel-configure-input.md)<br/> Contiene datos de entrada [**para el método IDirect3DAuthenticatedChannel9::Configure.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)<br/>                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURE \_ OUTPUT**](d3dauthenticatedchannel-configure-output.md)<br/> Contiene la respuesta a una llamada al [**método IDirect3DAuthenticatedChannel9::Configure.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)<br/>                                                                                                        |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREINITIALIZE**](d3dauthenticatedchannel-configureinitialize.md)<br/> Contiene datos de entrada para [**un comando D3DAUTHENTICATEDCONFIGURE \_ INITIALIZE.**](d3dauthenticatedconfigure-initialize.md)<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREPROTECTION**](d3dauthenticatedchannel-configureprotection.md)<br/> Contiene datos de entrada para [**un comando D3DAUTHENTICATEDCONFIGURE \_ PROTECTION.**](d3dauthenticatedconfigure-protection.md)<br/>                                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURECRYPTOSESSION**](d3dauthenticatedchannel-configurecryptosession.md)<br/> Contiene datos de entrada para [**un comando \_ CRYPTOSESSION D3DAUTHENTICATEDCONFIGURE.**](d3dauthenticatedconfigure-cryptosession.md)<br/>                                                                                                           |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGURESHAREDRESOURCE**](d3dauthenticatedchannel-configuresharedresource.md)<br/> Contiene datos de entrada para [**un comando D3DAUTHENTICATEDCONFIGURE \_ SHAREDRESOURCE.**](d3dauthenticatedconfigure-sharedresource.md)<br/>                                                                                                       |
| [**D3DAUTHENTICATEDCHANNEL \_ CONFIGUREUNCOMPRESSEDENCRYPTION**](d3dauthenticatedchannel-configureuncompressedencryption.md)<br/> Contiene datos de entrada para [**un comando D3DAUTHENTICATEDCONFIGURE \_ ENCRYPTIONWHENACCESSIBLE.**](d3dauthenticatedconfigure-encryptionwhenaccessible.md)<br/>                                                                   |
| [**MARCAS DE PROTECCIÓN D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-protection-flags.md)<br/> Especifica el nivel de protección para el contenido de vídeo.<br/>                                                                                                                                                                                                   |
| [**ENTRADA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-input.md)<br/> Contiene datos de entrada para [**el método IDirect3DAuthenticatedChannel9::Query.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)<br/>                                                                                                                                     |
| [**SALIDA DE CONSULTA D3DAUTHENTICATEDCHANNEL \_ \_**](d3dauthenticatedchannel-query-output.md)<br/> Contiene la respuesta a una llamada al método [**IDirect3DAuthenticatedChannel9::Query.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)<br/>                                                                                                                        |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYCHANNELTYPE \_ OUTPUT**](d3dauthenticatedchannel-querychanneltype-output.md)<br/> Contiene la respuesta a una [**consulta \_ CHANNELTYPE D3DAUTHENTICATEDQUERY.**](d3dauthenticatedquery-channeltype.md)<br/>                                                                                                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_ INPUT**](d3dauthenticatedchannel-querycryptosession-input.md)<br/> Contiene datos de entrada para una [**consulta \_ CRYPTOSESSION D3DAUTHENTICATEDQUERY.**](d3dauthenticatedquery-cryptosession.md)<br/>                                                                                                                |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYCRYPTOSESSION \_ OUTPUT**](d3dauthenticatedchannel-querycryptosession-output.md)<br/> Contiene la respuesta a una [**consulta \_ CRYPTOSESSION D3DAUTHENTICATEDQUERY.**](d3dauthenticatedquery-cryptosession.md)<br/>                                                                                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYDEVICEHANDLE \_ OUTPUT**](d3dauthenticatedchannel-querydevicehandle-output.md)<br/> Contiene la respuesta a una [**consulta \_ DEVICEHANDLE D3DAUTHENTICATEDQUERY.**](d3dauthenticatedquery-devicehandle.md)<br/>                                                                                                                 |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_ INPUT**](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)<br/> Contiene datos de entrada para una [**consulta D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID.**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)<br/>                                                                |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUID \_ OUTPUT**](d3dauthenticatedchannel-queryevictionencryptionguid-output.md)<br/> Contiene la respuesta a una [**consulta D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID.**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)<br/>                                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYEVICTIONENCRYPTIONGUIDCOUNT \_ OUTPUT**](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md)<br/> Contiene la respuesta a una [**consulta D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT.**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)<br/>                                         |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYINFOBUSTYPE \_ OUTPUT**](d3dauthenticatedchannel-queryinfobustype-output.md)<br/> Contiene la respuesta a una [**consulta D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES.**](d3dauthenticatedquery-accessibilityattributes.md)<br/>                                                                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_ INPUT**](d3dauthenticatedchannel-queryoutputid-input.md)<br/> Contiene datos intput para una [**consulta \_ OUTPUTID D3DAUTHENTICATEDQUERY.**](d3dauthenticatedquery-outputid.md)<br/>                                                                                                                                   |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTID \_ OUTPUT**](d3dauthenticatedchannel-queryoutputid-output.md)<br/> Contiene la respuesta a una [**consulta \_ OUTPUTID D3DAUTHENTICATEDQUERY.**](d3dauthenticatedquery-outputid.md)<br/>                                                                                                                                 |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ INPUT**](d3dauthenticatedchannel-queryoutputidcount-input.md)<br/> Contiene datos de entrada para una [**consulta D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT.**](d3dauthenticatedquery-outputidcount.md)<br/>                                                                                                                |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYOUTPUTIDCOUNT \_ OUTPUT**](d3dauthenticatedchannel-queryoutputidcount-output.md)<br/> Contiene la respuesta a una [**consulta D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT.**](d3dauthenticatedquery-outputidcount.md)<br/>                                                                                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYPROTECTION \_ OUTPUT**](d3dauthenticatedchannel-queryprotection-output.md)<br/> Contiene la respuesta a una [**consulta D3DAUTHENTICATEDQUERY \_ PROTECTION.**](d3dauthenticatedquery-protection.md)<br/>                                                                                                                         |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ INPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)<br/> Contiene datos de entrada para una [**consulta D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS.**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)<br/>                                        |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESS \_ OUTPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md)<br/> Contiene la respuesta a una [**consulta D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS.**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)<br/>                                     |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYRESTRICTEDSHAREDRESOURCEPROCESSCOUNT \_ OUTPUT**](d3dauthenticatedchannel-queryrestrictedsharedresourceprocesscount-output.md)<br/> Contiene la respuesta a una [**consulta D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT.**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)<br/>                 |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYUNCOMPRESSEDENCRYPTIONLEVEL \_ OUTPUT**](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md)<br/> Contiene la respuesta a una [**consulta D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE.**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)<br/>                                             |
| [**D3DAUTHENTICATEDCHANNEL \_ QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT \_ OUTPUT**](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md)<br/> Contiene la respuesta a una [**consulta D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT.**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md)<br/> |
| [**D3DCONTENTPROTECTIONCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcontentprotectioncaps)<br/> Describe las funcionalidades de protección de contenido de un controlador de pantalla.<br/>                                                                                                                                                                                                                    |
| [**INFORMACIÓN DE BLOQUES D3DENCRYPTED \_ \_**](d3dencrypted-block-info.md)<br/> Especifica qué bytes se cifran en una superficie de vídeo protegida.<br/>                                                                                                                                                                                                                     |
| [**D3DOVERLAYCAPS**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3doverlaycaps)<br/> Especifica las funcionalidades de superposición de hardware para un dispositivo Direct3D.<br/>                                                                                                                                                                                                                                            |
| [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo)<br/> Especifica un búfer para el [**método IDirect3DDXVADevice9::Execute.**](idirect3ddxvadevice9-execute.md)<br/>                                                                                                                                                                                                  |
| [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo)<br/> Especifica los requisitos de las superficies comprimidas para la aceleración de vídeo de DirectX (DXVA).<br/>                                                                                                                                                                                                         |
| [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo)<br/> Especifica las dimensiones y el formato de píxel de las superficies sin comprimir para lacoding de vídeo DXVA.<br/>                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 




