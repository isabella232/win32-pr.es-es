---
description: Obtiene la información de tipo de un elemento.
ms.assetid: 9670f184-e8ba-4596-af6d-2967320dfd95
title: 'IWiaItem2:: GetItemType (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetItemType
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3bf177ddcc117cdfe21a1b9322a0e457cf899c0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809986"
---
# <a name="iwiaitem2getitemtype-method"></a>IWiaItem2:: GetItemType (método)

Obtiene la información de tipo de un elemento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetItemType(
  [out] LONG *pItemType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pItemType* \[ enuncia\]
</dt> <dd>

Tipo: **Long \** _

Recibe un puntero a un _ *Long** que contiene una combinación de marcas de tipo. Vea [**marcas de tipo de elemento de WIA**](-wia-wia-item-type-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Cada objeto [**IWiaItem2**](-wia-iwiaitem2.md) del árbol jerárquico de objetos asociados a un dispositivo de hardware de adquisición de imágenes de Windows (WIA) 2,0 tiene un tipo de datos específico. Los objetos de elemento representan carpetas y archivos. Las carpetas contienen objetos de archivo. Los objetos de archivo contienen datos adquiridos por el dispositivo, como imágenes y sonidos. Este método permite a las aplicaciones identificar el tipo de cualquier elemento en un árbol jerárquico de objetos de elemento en un dispositivo.

Un elemento puede tener más de un tipo. Por ejemplo, un elemento que representa un archivo de audio tendrá los atributos de tipo [**WiaItemTypeAudio**](-wia-wia-item-type-flags.md) \| **WiaItemTypeFile**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




