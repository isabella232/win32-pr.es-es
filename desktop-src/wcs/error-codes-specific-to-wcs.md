---
title: Códigos de error específicos de WCS
description: A continuación se muestra una lista de códigos de error que están relacionados específicamente con el uso de WCS 1.0.
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46127e27b0f0890e305fee65534b0cce743c086e9e89934797bf2b16b15e9f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814605"
---
# <a name="error-codes-specific-to-wcs"></a>Códigos de error específicos de WCS

A continuación se muestra una lista de códigos de error que están relacionados específicamente con el uso de WCS 1.0. Esto no significa que las funciones wcs devuelvan solo estos códigos de error. Esto significa que los códigos de la tabla siguiente solo los devuelven las funciones de WCS. También pueden devolver otros códigos de error de Win32 que se documentan en otra parte en la API Win32 del SDK de plataforma.

<dl> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>ERROR \_ AL ELIMINAR ICM \_ \_ XFORM
</dt> <dd>

No se pudo eliminar la transformación de color especificada.

</dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>ERROR \_ DUPLICATE \_ TAG
</dt> <dd>

La etiqueta de elemento de perfil de color especificada ya está presente en el perfil de color.

</dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ERROR \_ ICM \_ HABILITADO \_
</dt> <dd>

Image Color Management no está habilitado actualmente.

</dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERROR \_ \_ CMM NO VÁLIDO
</dt> <dd>

El nombre de archivo especificado no hace referencia a un módulo de administración de colores válido.

</dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERROR \_ ESPACIO DE COLORES NO \_ VÁLIDO
</dt> <dd>

El espacio de colores especificado no es válido.

</dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERROR \_ PERFIL NO \_ VÁLIDO
</dt> <dd>

El nombre de archivo especificado no hace referencia a un perfil de color válido.

</dd> <dt>

<span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>ERROR \_ INVALID \_ TRANSFORM 
</dt> <dd>

La transformación de color que se especificó no es una transformación de color válida.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>PERFIL \_ DE ERROR NO ASOCIADO AL \_ \_ \_ \_ DISPOSITIVO
</dt> <dd>

El perfil de color especificado no está asociado a ningún dispositivo.

</dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>NO SE \_ ENCONTRÓ EL PERFIL DE \_ \_ ERROR 
</dt> <dd>

No se encontró el nombre de archivo de perfil de color especificado. El nombre de archivo o la ruta de acceso son incorrectos.

</dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>NO \_ SE ENCONTRÓ LA ETIQUETA DE \_ \_ ERROR
</dt> <dd>

No se encontró la etiqueta de elemento de perfil de color especificada en el perfil de color.

</dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>ETIQUETA \_ DE ERROR NO \_ \_ PRESENTE
</dt> <dd>

No se pasó a la función una etiqueta de elemento de perfil de color necesaria para que la función se realizara correctamente.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos básicos de administración de colores](basic-color-management-concepts.md)
</dt> <dt>

[Constantes de WCS](wcs-constants.md)
</dt> </dl>

 

 




