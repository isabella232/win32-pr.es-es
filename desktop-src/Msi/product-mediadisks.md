---
description: La propiedad MediaDisks enumera todos los discos multimedia de esta instancia de producto. Esta propiedad llama a MsiSourceListEnumMediaDisks. Devuelve la información del disco como una matriz de objetos Record.
ms.assetid: 9ea7c9a8-4ff1-4b26-a8d5-c23510650566
title: Propiedad Product.MediaDisks
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
ms.openlocfilehash: 00496739c9e51b5a735bf57788cdc47be0c41e177201ef445f58ea3748fb062f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042205"
---
# <a name="productmediadisks-property"></a>Propiedad Product.MediaDisks

La **propiedad MediaDisks** enumera todos los discos multimedia de esta instancia de producto. Esta propiedad llama a [**MsiSourceListEnumMediaDisks.**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa) Devuelve la información del disco como una matriz de [**objetos Record.**](record-object.md)

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Product.MediaDisks
```



## <a name="property-value"></a>Valor de propiedad

## <a name="remarks"></a>Comentarios

En cada registro, el primer campo contiene el identificador de disco, el segundo campo contiene la etiqueta del volumen y el tercer campo contiene el mensaje de disco registrado para el disco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct se define como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Producto**](product-object.md)
</dt> <dt>

[**MsiSourceListEnumMediaDisks**](/windows/desktop/api/Msi/nf-msi-msisourcelistenummediadisksa)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




