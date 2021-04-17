---
title: Códigos de error específicos de WCS
description: A continuación se muestra una lista de códigos de error que están relacionados específicamente con el uso de WCS 1,0.
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3040f462ce226ebd3018070abc818884cee6ad6
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/02/2021
ms.locfileid: "105721159"
---
# <a name="error-codes-specific-to-wcs"></a>Códigos de error específicos de WCS

A continuación se muestra una lista de códigos de error que están relacionados específicamente con el uso de WCS 1,0. Esto no significa que las funciones WCS devolverán solo estos códigos de error. Significa que los códigos de la tabla siguiente solo se devuelven mediante funciones WCS. También pueden devolver otros códigos de error de Win32 que se documentan en otro lugar de la API Win32 del SDK de la plataforma.

<dl> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>ERROR al \_ eliminar \_ el \_ XForm ICM
</dt> <dd>

No se pudo eliminar la transformación de color especificada.

</dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>ERROR \_ de \_ etiqueta duplicada
</dt> <dd>

La etiqueta del elemento de Perfil de color especificada ya está presente en el perfil de color.

</dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ERROR \_ ICM \_ no \_ habilitado
</dt> <dd>

La administración del color de imagen no está habilitada actualmente.

</dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERROR \_ de \_ CMM no válido
</dt> <dd>

El nombre de archivo especificado no hace referencia a un módulo de administración de color válido.

</dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERROR \_ COLORSPACE no válido \_
</dt> <dd>

El espacio de colores especificado no es válido.

</dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERROR \_ de \_ perfil no válido
</dt> <dd>

El nombre de archivo especificado no hace referencia a un perfil de color válido.

</dd> <dt>

<span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>ERROR \_ de \_ transformación no válida 
</dt> <dd>

La transformación de color que se especificó no es una transformación de color válida.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>\_perfil \_ de error no \_ asociado con el \_ \_ dispositivo
</dt> <dd>

El perfil de color especificado no está asociado a ningún dispositivo.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>\_ \_ no \_ se encontró el perfil de error 
</dt> <dd>

No se encontró el nombre de archivo del perfil de color especificado. El nombre de archivo o la ruta de acceso no son correctos.

</dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>\_ \_ no \_ se encontró la etiqueta de error
</dt> <dd>

No se encontró la etiqueta de elemento de Perfil de color especificada en el perfil de color.

</dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>etiqueta de ERROR \_ \_ no \_ presente
</dt> <dd>

No se pasó a la función una etiqueta de elemento de Perfil de color necesaria para que la función se ejecute correctamente.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de la administración del color](basic-color-management-concepts.md)
</dt> <dt>

[Constantes de WCS](wcs-constants.md)
</dt> </dl>

 

 




