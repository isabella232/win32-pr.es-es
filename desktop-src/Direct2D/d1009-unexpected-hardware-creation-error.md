---
title: D1009 Error inesperado de creación de hardware
description: Se encontró un error inesperado \error\ al intentar crear un destino de Direct3D.
ms.assetid: 1ff34b1f-0ab3-4821-97f5-a4e67831383a
keywords:
- D1009 Error inesperado de creación de hardware Direct2D
topic_type:
- apiref
api_name:
- D1009 Unexpected Hardware Creation Error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa51d2536995feb51081134e412d94617f34d069
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164158"
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

 

 




