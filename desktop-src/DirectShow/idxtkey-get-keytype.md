---
description: El \_ método get KeyType recupera el tipo de clave.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'Método IDxtKey:: get_KeyType (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7341815169549f24db55518e021b9e5096286a65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679421"
---
# <a name="idxtkeyget_keytype-method"></a>IDxtKey:: get \_ KeyType (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `get_KeyType` método recupera el tipo de clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Recibe uno de los siguientes valores de enumeración.



| Value             | Descripción                                           |
|-------------------|-------------------------------------------------------|
| DXTKEY \_ RGB       | Clave cromada. (Clave en valor RGB).                       |
| DXTKEY \_ NONRED    | Clave Nonred. (Hace que las áreas azules y verdes sean transparentes). |
| \_luminancia DXTKEY | Clave de luminancia.                                        |
| \_alfa DXTKEY     | Clave por valor alfa.                                   |
| \_matiz DXTKEY       | Clave por matiz.                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IDxtKey**](idxtkey.md)
</dt> </dl>

 

 




