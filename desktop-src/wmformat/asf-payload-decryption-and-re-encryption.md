---
title: Descifrado y volver a cifrar la carga de ASF
description: Descifrado y volver a cifrar la carga de ASF
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- Windows SDK de formato multimedia, descifrado de carga de ASF y nuevo cifrado
- Windows SDK de formato multimedia, descifrado de carga y nuevo cifrado
- Windows SDK de formato multimedia, descifrado
- Windows SDK de formato multimedia, volver a cifrar
- administración de derechos digitales (DRM), descifrado de carga de ASF y nuevo cifrado
- DRM (administración de derechos digitales), descifrado de carga de ASF y nuevo cifrado
- administración de derechos digitales (DRM), descifrado de carga y nuevo cifrado
- DRM (administración de derechos digitales), descifrado de carga y nuevo cifrado
- administración de derechos digitales (DRM),descifrado
- DRM (administración de derechos digitales),descifrado
- administración de derechos digitales (DRM), volver a cifrar
- DRM (administración de derechos digitales), volver a cifrar
- API extendidas de cliente DRM, descifrado de carga de ASF y nuevo cifrado
- API extendidas de cliente, descifrado de carga de ASF y nuevo cifrado
- API extendidas de cliente DRM, descifrado de carga y nuevo cifrado
- API extendidas de cliente, descifrado de carga y nuevo cifrado
- API extendidas de cliente DRM, descifrado
- API extendidas de cliente, descifrado
- API extendidas de cliente DRM, volver a cifrar
- API extendidas de cliente, volver a cifrar
- Formato de sistemas avanzados (ASF), volver a cifrar
- ASF (formato de sistemas avanzados), volver a cifrar
- Formato de sistemas avanzados (ASF), descifrado
- ASF (formato de sistemas avanzados),descifrado
- Formato de sistemas avanzados (ASF), descifrado de carga y nuevo cifrado
- ASF (formato de sistemas avanzados), descifrado de carga útil y nuevo cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c6dcab1d483b737b6b05636b51b8af0502350
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359580"
---
# <a name="asf-payload-decryption-and-re-encryption"></a>Descifrado y volver a cifrar la carga de ASF

Los pasos siguientes describen las acciones que una aplicación debe completar para descifrar y volver a cifrar cada carga:

1.  Incremente el valor de sal.
2.  Pase la carga (cifrada con drm multimedia de Windows) y el valor salt a la función de [**descifrado, IWMDRMDecrypt::D ecrypt**](iwmdrmdecrypt-decrypt.md), que devolverá la carga, cifrada con la clave pública RC4.
3.  Derive una clave RC4 transitoria aplicando un hash SHA-1 del vector de inicialización concatenado con el valor salt.
4.  Use la clave transitoria para descifrar la carga.
5.  Vuelva a cifrar inmediatamente la carga con el esquema de protección de contenido autorizado según las Windows de cumplimiento y solidez de la exportación de DRM multimedia.
6.  Busque la siguiente carga.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Exportar contenido comprimido**](exporting-compressed-content.md)
</dt> </dl>

 

 




