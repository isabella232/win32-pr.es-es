---
title: Archivos de biblioteca, archivos de encabezado y archivos del compilador Configuración
description: Archivos de biblioteca, archivos de encabezado y archivos del compilador Configuración
ms.assetid: 7563bb3a-7bea-4e0c-8205-a16b276c8d1e
keywords:
- Windows SDK de formato multimedia, archivos de biblioteca DRM
- Windows SDK de formato multimedia, archivos de biblioteca
- Windows SDK de formato multimedia, archivos de encabezado DRM
- Windows SDK de formato multimedia, archivos de encabezado
- Windows SDK de formato multimedia, configuración del compilador DRM
- Windows SDK de formato multimedia, configuración del compilador
- administración de derechos digitales (DRM),archivos de biblioteca
- DRM (administración de derechos digitales),archivos de biblioteca
- administración de derechos digitales (DRM), archivos de encabezado
- DRM (administración de derechos digitales), archivos de encabezado
- administración de derechos digitales (DRM), configuración del compilador
- DRM (administración de derechos digitales), configuración del compilador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 537742e40778120ff1b712b2170a1c451f7598b935717a574048b619321fa96d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084742"
---
# <a name="library-files-header-files-and-compiler-settings"></a>Archivos de biblioteca, archivos de encabezado y archivos del compilador Configuración

Los componentes de programación de Windows Media DRM Client Extended API se definen en el archivo de encabezado wmdrmsdk.h y se implementan en las bibliotecas wmdrmsdk.lib y mfuuid.lib.

Algunas de las funcionalidades de las API extendidas Windows de cliente DRM multimedia requieren que obtenga una biblioteca protegida de Microsoft. Esta biblioteca, denominada biblioteca de código auxiliar en esta documentación, es específica del destinatario y especifica el nivel de seguridad de la aplicación para las aplicaciones. La biblioteca de código auxiliar reemplaza wmdrmsdk.lib; nunca debe vincular a ambos.

**Nota** La biblioteca de código auxiliar DRM es independiente de la biblioteca de código auxiliar que usa el resto del SDK de formato multimedia de Windows, pero tiene licencia con el mismo método.

**Nota** La biblioteca de código auxiliar drm debe vincularse a la aplicación después del archivo de biblioteca msvcrt.lib para evitar errores del enlazador.

La biblioteca de código auxiliar contiene un certificado incrustado que Microsoft puede revocar si no cumple los términos y condiciones del contrato de licencia.

Los métodos específicos que requieren la biblioteca de código auxiliar se etiquetan en la documentación. Si intenta usar este tipo de método sin vincular a la biblioteca de código auxiliar, devolverá un error NS \_ E \_ DRM \_ STUBLIB \_ REQUIRED.

El subsistema DRM no se puede usar en una compilación de depuración. Si se intenta, los métodos de la API devolverán el error NS \_ E \_ DRM \_ DEBUGGING NOT \_ \_ ALLOWED.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas iniciales**](drm-getting-started.md)
</dt> <dt>

[**Archivos de biblioteca y archivos del compilador Configuración**](library-files-and-compiler-settings.md)
</dt> <dt>

[**Obtención de la biblioteca DRM requerida**](obtaining-the-required-drm-library.md)
</dt> </dl>

 

 




