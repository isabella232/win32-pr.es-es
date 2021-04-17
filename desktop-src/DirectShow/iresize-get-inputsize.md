---
description: El \_ método get Inlocate devuelve el tamaño de entrada actual del filtro de tamaño.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: 'Método IResize:: get_InputSize (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fab61edf6dc4469f06437483172161fbbe77e76d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681023"
---
# <a name="iresizeget_inputsize-method"></a>IResize:: get \_ Inlocate (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `get_InputSize` método devuelve el tamaño de entrada actual del filtro de tamaño.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*piHeight* \[ enuncia\]
</dt> <dd>

Recibe el alto del vídeo, en píxeles.

</dd> <dt>

*piWidth* \[ enuncia\]
</dt> <dd>

Recibe el ancho del vídeo, en píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Si el PIN de entrada del filtro no está conectado, devuelva un código de error. De lo contrario, devuelva el ancho y el alto del vídeo, según lo especificado por el tipo de medio del PIN de entrada.

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | DirectX 9,0 o posterior<br/>                                                         |
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> <dt>

[**Interfaz IResize**](iresize.md)
</dt> </dl>

 

 




