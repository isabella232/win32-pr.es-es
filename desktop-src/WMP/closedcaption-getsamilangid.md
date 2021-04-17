---
title: ClosedCaption. getSAMILangID, método
description: El método getSAMILangID recupera el identificador de configuración regional (LCID) de un idioma admitido por el archivo SAMI actual.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- método getSAMILangID de Windows Media Player
- método getSAMILangID de Windows Media Player, clase ClosedCaption
- Clase ClosedCaption Windows Media Player, método getSAMILangID
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd543c9cb9d884022d78a875a2f8de078c479b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700429"
---
# <a name="closedcaptiongetsamilangid-method"></a>ClosedCaption. getSAMILangID, método

El método **getSAMILangID** recupera el identificador de configuración regional (LCID) de un idioma admitido por el archivo Sami actual.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ de de\]
</dt> <dd>

**Número** (**largo**) que especifica el índice del LCID que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número** (**Long**) que contiene el LCID del idioma con el índice especificado.

## <a name="remarks"></a>Observaciones

Los idiomas de un archivo SAMI se indizan en el orden mostrado en el archivo, empezando por cero.

Este método no se puede usar hasta que se abra un archivo multimedia digital (*reproductor*.**openState** es igual a 13).

**Windows Media Player 10 Mobile:** Este método no se admite.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/>                                 |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Objeto ClosedCaption**](closedcaption-object.md)
</dt> </dl>

 

 





