---
description: El método put \_ Similarity especifica el intervalo de datos de color que se vuelve transparente. En valores más altos, una gama más amplia de colores similares es transparente. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB o DXTKEY \_ NONRED.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: Método IDxtKey::p ut_Similarity (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361326"
---
# <a name="idxtkeyput_similarity-method"></a>Método IDxtKey::p ut \_ Similarity

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `put_Similarity` método especifica el intervalo de datos de color que se vuelve transparente. En valores más altos, una gama más amplia de colores similares es transparente. Esta propiedad solo se aplica cuando el tipo de clave es DXTKEY \_ RGB o DXTKEY \_ NONRED.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ En\]
</dt> <dd>

Especifica el valor de similitud. El intervalo válido es de 0 a 100.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDxtKey (interfaz)**](idxtkey.md)
</dt> <dt>

[**IDxtKey::put \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




