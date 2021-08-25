---
description: Enumera las consultas para el método IDirect3DAuthenticatedChannel9::Query.
ms.assetid: 75e246c6-bf23-44d9-8fb3-46a6dc5324a5
title: Content Protection consultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5aaa8c43cf722d13550ab4a1860e7a53780e7e82da7f374e28a7f599a22638
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829095"
---
# <a name="content-protection-queries"></a>Content Protection consultas

Enumera las consultas para el [**método IDirect3DAuthenticatedChannel9::Query.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)



| Solicitud de estado                                                                                                                            | Descripción                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DAUTHENTICATEDQUERY \_ ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md)                                   | Devuelve el tipo de bus de E/S usado para enviar datos a la GPU.                                                                                                   |
| [**D3DAUTHENTICATEDQUERY \_ CHANNELTYPE**](d3dauthenticatedquery-channeltype.md)                                                           | Devuelve el tipo de canal autenticado.                                                                                                                  |
| [**D3DAUTHENTICATEDQUERY \_ CRYPTOSESSION**](d3dauthenticatedquery-cryptosession.md)                                                       | Devuelve identificadores a la sesión criptográfica y al dispositivo Direct3D que están asociados a un dispositivo descodificador de Aceleración de vídeo 2 (DXVA-2) de DirectX especificado. |
| [**D3DAUTHENTICATEDQUERY \_ CURRENTENCRYPTIONWHENACCESSIBLE**](d3dauthenticatedquery-currentencryptionwhenaccessible.md)                   | Devuelve el tipo de cifrado que se aplica antes de que el contenido sea accesible para la CPU o el bus.                                                            |
| [**D3DAUTHENTICATEDQUERY \_ DEVICEHANDLE**](d3dauthenticatedquery-devicehandle.md)                                                         | Devuelve un identificador al dispositivo asociado a este canal autenticado.                                                                          |
| [**CIFRADO D3DAUTHENTICATEDQUERYWHENACCESSIBLEGUID \_**](d3dauthenticatedquery-encryptionwhenaccessibleguid.md)                         | Devuelve uno de los tipos de cifrado que se pueden usar para cifrar el contenido antes de que sea accesible para la CPU o el bus.                                     |
| [**CIFRADO D3DAUTHENTICATEDQUERYWHENACCESSIBLEGUIDCOUNT \_**](d3dauthenticatedquery-encryptionwhenaccessibleguidcount.md)               | Devuelve el número de tipos de cifrado que se pueden usar para cifrar el contenido antes de que sea accesible para la CPU o el bus.                                  |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTID**](d3dauthenticatedquery-outputid.md)                                                                 | Devuelve uno de los identificadores de salida asociados a una sesión criptográfica y un dispositivo Direct3D especificados.                                        |
| [**D3DAUTHENTICATEDQUERY \_ OUTPUTIDCOUNT**](d3dauthenticatedquery-outputidcount.md)                                                       | Devuelve el número de identificadores de salida asociados a una sesión criptográfica y un dispositivo Direct3D especificados.                                             |
| [**D3DAUTHENTICATEDQUERY \_ PROTECTION**](d3dauthenticatedquery-protection.md)                                                             | Devuelve el nivel de protección actual del dispositivo.                                                                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md)                   | Devuelve información sobre un proceso que puede abrir recursos compartidos con acceso restringido.                                                        |
| [**D3DAUTHENTICATEDQUERY \_ RESTRICTEDSHAREDRESOURCEPROCESSCOUNT**](d3dauthenticatedquery-restrictedsharedresourceprocesscount.md)         | Devuelve el número de procesos que pueden abrir recursos compartidos con acceso restringido.                                                           |
| [**D3DAUTHENTICATEDQUERY \_ UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**](d3dauthenticatedquery-unrestrictedprotectedsharedresourcecount.md) | Devuelve el número de recursos compartidos protegidos que puede abrir cualquier proceso sin restricciones.                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de vídeo de Direct3D](direct3d-video-apis.md)
</dt> <dt>

[Datos basados en GPU Content Protection](gpu-based-content-protection.md)
</dt> </dl>

 

 



