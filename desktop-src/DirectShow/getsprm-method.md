---
description: El método GetSPRM recupera el registro de parámetros del sistema especificado.
ms.assetid: c6177f43-2809-4ef2-bc94-ac9a28f94621
title: Método GetSPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8b6898902eda55e0e877878343a25d82d03660
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061106"
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

Especifica el registro cuyo valor desea recuperar como entero. El entero debe oscilar entre 0 y 23.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el contenido del registro especificado.

## <a name="remarks"></a>Observaciones

El disco controla los registros de parámetros del sistema (SPRM). Una aplicación de reproductor no necesita acceder a estos registros para ninguna funcionalidad de navegación estándar. Los SPRM representan el estado del reproductor. Cada uno tiene un significado, establecido por preferencias de usuario, comandos de disco y otras repeticiones sobre las que una aplicación no tiene control directo. Una aplicación puede leer estos registros, pero no puede escribir en ellos. Para usar estos registros de forma eficaz, probablemente necesitará un conocimiento más detallado de los comandos de navegación de DVD que se proporciona en esta documentación. En la tabla siguiente se muestra el contenido de cada registro. Para obtener información más detallada sobre el contenido del registro, vea [ **IDvdInfo2::GetAllSPRMs.**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getallsprms)



| Registrarse | Contenido                        |
|----------|---------------------------------|
| 0        | Código de idioma del menú              |
| 1        | Número de secuencia de audio             |
| 2        | Número de secuencia de subimagen        |
| 3        | Número de ángulo actual            |
| 4        | Número de título actual            |
| 5        | Número de título                    |
| 6        | Número PGC                      |
| 7        | Número de capítulo actual (PTT)    |
| 8        | Número de botón resaltado       |
| 9        | Temporizador de navegación                |
| 10       | Salto PGC para navegación. timer         |
| 11       | Modo de presentación audio audio de audio |
| 12       | Código de país o región de PML         |
| 13       | PML                             |
| 14       | Configuración de vídeo                   |
| 15       | Funcionalidad de audio                |
| 16       | Idioma de audio                  |
| 17       | Extensión de lenguaje de audio        |
| 18       | Lenguaje de subimagen             |
| 19       | Extensión de lenguaje de subimagen   |
| 20       | Código de región del reproductor              |
| 21       | Reservada                        |
| 22       | Reservada                        |
| 23       | Reservada                        |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**GetGPRM**](getgprm-method.md)
</dt> <dt>

[**SetGPRM**](setgprm-method.md)
</dt> </dl>

 

 



