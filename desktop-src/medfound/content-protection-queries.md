---
description: 'Muestra las consultas para el método IDirect3DAuthenticatedChannel9:: query.'
ms.assetid: 75e246c6-bf23-44d9-8fb3-46a6dc5324a5
title: Consultas Content Protection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a72f7f054783a644cb352727f4bf65864bf5f8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714934"
---
# <a name="content-protection-queries"></a>Consultas Content Protection

Muestra las consultas para el método [**IDirect3DAuthenticatedChannel9:: query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query) .



| Solicitud de estado                                                                                                                            | Descripción                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md)                                   | Devuelve el tipo de bus de e/s que se usa para enviar datos a la GPU.                                                                                                   |
| [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md)                                                           | Devuelve el tipo de canal autenticado.                                                                                                                  |
| [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md)                                                       | Devuelve los identificadores de la sesión criptográfica y el dispositivo Direct3D que están asociados a un dispositivo descodificador DirectX video Acceleration 2 (DXVA-2) especificado. |
| [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)                   | Devuelve el tipo de cifrado que se aplica antes de que el contenido sea accesible para la CPU o el bus.                                                            |
| [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md)                                                         | Devuelve un identificador para el dispositivo que está asociado a este canal autenticado.                                                                          |
| [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUID**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)                         | Devuelve uno de los tipos de cifrado que se pueden usar para cifrar el contenido antes de que sea accesible para la CPU o el bus.                                     |
| [**D3DAUTHENTICATEDQUERY \_ ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)               | Devuelve el número de tipos de cifrado que se pueden usar para cifrar el contenido antes de que sea accesible para la CPU o el bus.                                  |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md)                                                                 | Devuelve uno de los identificadores de salida que está asociado a una sesión criptográfica y un dispositivo Direct3D especificados.                                        |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md)                                                       | Devuelve el número de identificadores de salida asociados a una sesión criptográfica y un dispositivo Direct3D especificados.                                             |
| [**Protección de D3DAUTHENTICATEDQUERY \_**](d3dauthenticatedquery-protection.md)                                                             | Devuelve el nivel de protección actual del dispositivo.                                                                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)                   | Devuelve información sobre un proceso que puede abrir recursos compartidos con acceso restringido.                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)         | Devuelve el número de procesos que pueden abrir recursos compartidos con acceso restringido.                                                           |
| [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) | Devuelve el número de recursos compartidos protegidos que puede abrir cualquier proceso sin restricciones.                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D](direct3d-video-apis.md)
</dt> <dt>

[Content Protection basados en GPU](gpu-based-content-protection.md)
</dt> </dl>

 

 



