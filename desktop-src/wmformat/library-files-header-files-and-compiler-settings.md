---
title: Archivos de biblioteca, archivos de encabezado y configuración del compilador
description: Archivos de biblioteca, archivos de encabezado y configuración del compilador
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- SDK de Windows Media Format, archivos de biblioteca DRM
- SDK de Windows Media Format, archivos de biblioteca
- SDK de Windows Media Format, archivos de encabezado DRM
- Windows Media Format SDK, archivos de encabezado
- SDK de Windows Media Format, configuración del compilador DRM
- SDK de Windows Media Format, configuración del compilador
- Administración de derechos digitales (DRM), archivos de biblioteca
- DRM (administración de derechos digitales), archivos de biblioteca
- Administración de derechos digitales (DRM), archivos de encabezado
- DRM (administración de derechos digitales), archivos de encabezado
- Administración de derechos digitales (DRM), configuración del compilador
- DRM (administración de derechos digitales), configuración del compilador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b0b10ea03cc08d5b689b74f9c647f7d0138fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104148822"
---
# <a name="library-files-header-files-and-compiler-settings"></a>Archivos de biblioteca, archivos de encabezado y configuración del compilador

Los componentes de programación de las API extendidas del cliente DRM de Windows Media se definen en el archivo de encabezado wmdrmsdk. h y se implementan en las bibliotecas wmdrmsdk. lib y mfuuid. lib.

Parte de la funcionalidad de las API extendidas del cliente DRM de Windows Media requiere la obtención de una biblioteca protegida de Microsoft. Esta biblioteca, denominada Biblioteca de código auxiliar en esta documentación, es específica del destinatario y especifica el nivel de seguridad de la aplicación para las aplicaciones. La biblioteca de código auxiliar reemplaza a wmdrmsdk. lib; nunca debe vincularse a ambos.

**Nota:** La biblioteca de código auxiliar de DRM es independiente de la biblioteca de código auxiliar usada por el resto del SDK de Windows Media Format, pero tiene licencia mediante el mismo método.

**Nota:** La biblioteca de rutas de DRM debe estar vinculada en la aplicación después del archivo de biblioteca msvcrt. lib para evitar errores del vinculador.

La biblioteca de código auxiliar contiene un certificado incrustado que Microsoft puede revocar si no cumple con los términos y condiciones del contrato de licencia.

Los métodos específicos que requieren la biblioteca de código auxiliar se etiquetan en la documentación de. Si intenta utilizar este tipo de método sin vincular a la biblioteca de código auxiliar, devolverá un error de STUBLIB de DRM de NS \_ E \_ DRM \_ \_ .

El subsistema DRM no se puede usar en una compilación de depuración. Si se intenta esto, los métodos de la API devolverán \_ el \_ error de depuración de DRM de NS E \_ \_ no \_ permitido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción**](drm-getting-started.md)
</dt> <dt>

[**Archivos de biblioteca y configuración del compilador**](library-files-and-compiler-settings.md)
</dt> <dt>

[**Obtención de la biblioteca DRM necesaria**](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




