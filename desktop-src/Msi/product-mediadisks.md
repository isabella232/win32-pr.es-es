---
description: La propiedad MediaDisks enumera todos los discos multimedia para esta instancia de producto. Esta propiedad llama a MsiSourceListEnumMediaDisks. Devuelve la información del disco como una matriz de objetos de registro.
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: Propiedad product. MediaDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.MediaDisks
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e07af832837aaeb77759816c08cf68d04e14c255
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653424"
---
# <a name="productmediadisks-property"></a>Propiedad product. MediaDisks

La propiedad **MediaDisks** enumera todos los discos multimedia para esta instancia de producto. Esta propiedad llama a [**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa). Devuelve la información del disco como una matriz de objetos de [**registro**](record-object.md) .

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Observaciones

En cada registro, el primer campo contiene el ID. de disco, el segundo campo contiene la etiqueta de volumen y el tercer campo contiene el símbolo del sistema registrado para el disco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Manuales**](product-object.md)
</dt> <dt>

[**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




