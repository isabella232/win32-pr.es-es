---
description: El método GetConnectedMediaType recupera el tipo de medio para la conexión en el PIN de entrada del enganche de ejemplo.
ms.assetid: 65f5603a-1151-4ffd-a662-84e265663b04
title: 'ISampleGrabber:: GetConnectedMediaType (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetConnectedMediaType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 85e30820afdca865f438ac40521a9be540fd4a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679066"
---
# <a name="isamplegrabbergetconnectedmediatype-method"></a>ISampleGrabber:: GetConnectedMediaType (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetConnectedMediaType` método recupera el tipo de medio para la conexión en el PIN de entrada del enganche de ejemplo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConnectedMediaType(
   AM_MEDIA_TYPE *pType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pType* 
</dt> <dd>

Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) asignada por el llamador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores siguientes.



| Código devuelto                                                                                           | Descripción                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**\_puntero E**</dt> </dl>             | Argumento de puntero **nulo** .<br/>   |
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Correcto.<br/>                     |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | El filtro no está conectado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método copia el tipo de medio en la estructura de **\_ \_ tipo de medio am** especificada por *pType*. El autor de la llamada debe liberar el bloque de formato del tipo de medio. Puede usar la función **CoTaskMemFree** o la función [**FreeMediaType**](freemediatype.md) en la biblioteca de clase base.

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

[Usar el enganche de ejemplo](using-the-sample-grabber.md)
</dt> <dt>

[**Interfaz ISampleGrabber**](isamplegrabber.md)
</dt> </dl>

 

 




