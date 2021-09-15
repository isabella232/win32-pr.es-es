---
description: Crea un objeto enumerador y devuelve un puntero a su interfaz IEnumWiaItem2 para carpetas con elementos en el árbol IWiaItem2 de un dispositivo de adquisición de imágenes de Windows (WIA) 2.0.
ms.assetid: 0862bb6f-0464-491a-8cad-60b92d9609f1
title: Método IWiaItem2::EnumChildItems (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumChildItems
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2de76d9bf43d10e08e5a85cd2a32d6b377680d18
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571341"
---
# <a name="iwiaitem2enumchilditems-method"></a>IWiaItem2::EnumChildItems (método)

Crea un objeto enumerador y devuelve un puntero a su interfaz [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) para carpetas con elementos en el árbol [**IWiaItem2**](-wia-iwiaitem2.md) de un dispositivo de adquisición de imágenes de Windows (WIA) 2.0.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumChildItems(
  [in]  const GUID          *pCategoryGUID,
  [out]       IEnumWiaItem2 **ppIEnumWiaItem2
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCategoryGUID* \[ En\]
</dt> <dd>

Tipo: **\* GUID const**

Especifica un puntero a una categoría para la que se enumeran los nodos secundarios. Si **es NULL,** se enumeran todos los nodos secundarios.

</dd> <dt>

*ppIEnumWiaItem2* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWiaItem2**](-wia-ienumwiaitem2.md)\*\***

Recibe la dirección de un puntero a la [**interfaz IEnumWiaItem2**](-wia-ienumwiaitem2.md) que este método crea.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

El sistema en tiempo de ejecución WIA 2.0 representa cada dispositivo de hardware WIA 2.0 como un árbol jerárquico de [**objetos IWiaItem2.**](-wia-iwiaitem2.md) El **método IWiaItem2::EnumChildItems permite** a las aplicaciones enumerar los elementos secundarios del elemento actual. Sin embargo, solo se puede aplicar a elementos que son carpetas.

Si la carpeta no está vacía, contiene un subárbol de [**objetos IWiaItem2.**](-wia-iwiaitem2.md) El **método IWiaItem2::EnumChildItems** enumera todos los elementos contenidos en la carpeta . Almacena un puntero a un enumerador en el *parámetro ppIEnumWiaItem2.* Las aplicaciones usan el puntero de enumerador para realizar la enumeración de los elementos secundarios de un objeto.

Las aplicaciones deben llamar [al método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en los punteros de interfaz que reciben a través del *parámetro ppIEnumWiaItem2.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
