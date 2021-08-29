---
title: Error de creación de hardware inesperado de D1009
description: Se encontró un error inesperado \error\ al intentar crear un destino de Direct3D.
ms.assetid: 1ff34b1f-0ab3-4821-97f5-a4e67831383a
keywords:
- Error de creación de hardware inesperado de D1009 Direct2D
topic_type:
- apiref
api_name:
- D1009 Unexpected Hardware Creation Error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eef3c09f5783f0011d5f2802b73948b13cc1c2075401a261ec96b015d50b2d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984025"
---
# <a name="d1009-unexpected-hardware-creation-error"></a>D1009: Error inesperado de creación de hardware

Se encontró un \[ *error inesperado* \] al intentar crear un destino de Direct3D.

## <a name="placeholders"></a>Marcadores de posición

<dl> <dt>

<span id="error"></span><span id="ERROR"></span>*Error*
</dt> <dd>

Número de error.

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Nivel de error | Advertencia |



 

## <a name="possible-causes"></a>Causas posibles

-   El destino era mayor que el tamaño máximo del mapa de bits.
-   Memoria de vídeo sin memoria cuando se crea el destino de representación.
-   No se pudo crear ningún dispositivo Direct3D.
-   La aplicación se ejecuta en IA64.

 

 




