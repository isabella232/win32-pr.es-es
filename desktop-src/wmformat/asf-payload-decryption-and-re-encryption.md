---
title: Descifrado y recifrado de carga ASF
description: Descifrado y recifrado de carga ASF
ms.assetid: 0a8c996d-2167-483a-93af-6fe22f0efaf1
keywords:
- SDK de Windows Media Format, descifrado de carga ASF y nuevo cifrado
- SDK de Windows Media Format, descifrado de carga y recifrado
- SDK de Windows Media Format, descifrado
- SDK de Windows Media Format, volver a cifrar
- Administración de derechos digitales (DRM), descifrado de carga ASF y recifrado
- DRM (administración de derechos digitales), descifrado de carga de ASF y recifrado
- Administración de derechos digitales (DRM), descifrado de carga y recifrado
- DRM (administración de derechos digitales), descifrado de carga y recifrado
- Administración de derechos digitales (DRM), descifrado
- DRM (administración de derechos digitales), descifrado
- Administración de derechos digitales (DRM), volver a cifrar
- DRM (administración de derechos digitales), volver a cifrar
- API extendidas del cliente DRM, descifrado de carga ASF y nuevo cifrado
- API extendidas de cliente, descifrado de carga ASF y recifrado
- API extendidas del cliente DRM, descifrado de carga y recifrado
- API extendidas de cliente, descifrado de carga y recifrado
- API extendidas del cliente DRM, descifrado
- API extendidas del cliente, descifrado
- API extendidas del cliente DRM, volver a cifrar
- API extendidas del cliente, volver a cifrar
- Advanced Systems Format (ASF), volver a cifrar
- ASF (formato de sistemas avanzados), volver a cifrar
- Advanced Systems Format (ASF), descifrado
- ASF (formato de sistemas avanzados), descifrado
- Advanced Systems Format (ASF), descifrado de carga y recifrado
- ASF (formato de sistemas avanzados), descifrado de carga y nuevo cifrado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313c6dcab1d483b737b6b05636b51b8af0502350
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773404"
---
# <a name="asf-payload-decryption-and-re-encryption"></a>Descifrado y recifrado de carga ASF

En los pasos siguientes se describen las acciones que una aplicación debe completar para descifrar y volver a cifrar cada carga:

1.  Incremente el valor Salt.
2.  Pase la carga (cifrada con DRM de Windows Media) y el valor Salt a la función de descifrado, [**IWMDRMDecrypt::D ECRYPT**](iwmdrmdecrypt-decrypt.md), que devolverá la carga cifrada mediante la clave pública RC4.
3.  Derive una clave RC4 transitoria aplicando un hash SHA-1 del vector de inicialización concatenado con el valor Salt.
4.  Use la clave transitoria para descifrar la carga.
5.  Vuelva a cifrar inmediatamente la carga con el esquema de protección de contenido autorizado según las reglas de compatibilidad y solidez de exportación de DRM de Windows Media.
6.  Busque la siguiente carga.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Exportar contenido comprimido**](exporting-compressed-content.md)
</dt> </dl>

 

 




