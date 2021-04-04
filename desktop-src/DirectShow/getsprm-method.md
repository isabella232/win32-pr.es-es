---
description: El método GetSPRM recupera el registro de parámetros del sistema especificado.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Método GetSPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103997646"
---
# <a name="getsprm-method"></a>Método GetSPRM

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

El `GetSPRM` método recupera el registro de parámetros del sistema especificado.

``` syntax
[ iSPRM = ] MSWebDVD.GetSPRM(iIndex)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*
</dt> <dd>

Especifica el registro cuyo valor se desea recuperar como un entero. El entero debe oscilar entre 0 y 23.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el contenido del registro especificado.

## <a name="remarks"></a>Observaciones

Los registros de parámetros del sistema de controles de disco (SPRMs). Una aplicación de reproducción no necesita tener acceso a estos registros para ninguna funcionalidad de navegación estándar. SPRMs representa el estado del reproductor. Cada una tiene un significado, establecido por las preferencias del usuario, los comandos del disco y otras repeticiones en las que una aplicación no tiene control directo. Una aplicación puede leer estos registros, pero no puede escribir en ellos. Para usar estos registros de forma eficaz, es probable que necesite un conocimiento más detallado de los comandos de navegación de DVD que los que se proporcionan en esta documentación. En la tabla siguiente se muestra el contenido de cada registro. Para obtener información más detallada sobre el contenido del registro, vea [ **IDvdInfo2:: GetAllSPRMs**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)



| Register | Contenido                        |
|----------|---------------------------------|
| 0        | Código de idioma del menú              |
| 1        | Número de secuencia de audio             |
| 2        | Número de secuencia de subimagen        |
| 3        | Número de ángulo actual            |
| 4        | Número de título actual            |
| 5        | Número de título                    |
| 6        | Número de PGC                      |
| 7        | Número de capítulo actual (PTT)    |
| 8        | Número de botón resaltado       |
| 9        | Temporizador de navegación                |
| 10       | Salto de PGC para NAV. timer         |
| 11       | Modo de presentación de audio de karaoke |
| 12       | Código de país o región de PML         |
| 13       | PML                             |
| 14       | Configuración de vídeo                   |
| 15       | Funcionalidad de audio                |
| 16       | Idioma de audio                  |
| 17       | Extensión de lenguaje de audio        |
| 18       | Idioma de subimagen             |
| 19       | Extensión de lenguaje de subimagen   |
| 20       | Código de región del reproductor              |
| 21       | Reservado                        |
| 22       | Reservado                        |
| 23       | Reservado                        |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetGPRM**](getgprm-method.md)
</dt> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



