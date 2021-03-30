---
description: La propiedad ButtonsAvailable recupera el número total de botones del menú actual.
ms.assetid: 4df3a7e7-1be4-4cc7-ad61-567f7f45811e
title: Propiedad ButtonsAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cab4afdd9f6e23a376bb72885810b8464f180d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423019"
---
# <a name="buttonsavailable-property"></a>Propiedad ButtonsAvailable

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `ButtonsAvailable` propiedad recupera el número total de botones del menú actual.

``` syntax
[ iButtons = ] MSWebDVD.ButtonsAvailable
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que representa el número de botones.

## <a name="remarks"></a>Observaciones

Esta propiedad es de solo lectura y no tiene ningún valor predeterminado. Use este método al implementar el control de mouse personalizado después de establecer [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) en **true**.

Llame a este método para recuperar el límite superior para el intervalo de números de botón válidos.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CurrentButton**](currentbutton-property.md)
</dt> <dt>

[**GetButtonAtPosition**](getbuttonatposition-method.md)
</dt> <dt>

[**GetButtonRect**](getbuttonrect-method.md)
</dt> <dt>

[**SelectAndActivateButton**](selectandactivatebutton-method.md)
</dt> <dt>

[**SelectAtPosition**](selectatposition-method.md)
</dt> </dl>

 

 



