---
description: El método TransAdd agrega una transición al objeto. Un objeto puede tener varias transiciones, pero no deben superponerse en el tiempo. Las transiciones deben estar dentro de los límites de tiempo del objeto.
ms.assetid: 2c3f923f-c754-4cc8-82ca-d3979d4bda07
title: 'IAMTimelineTransable:: TransAdd (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.TransAdd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2636922549635c4a1c5e6e0b36f308f62328dc60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690992"
---
# <a name="iamtimelinetransabletransadd-method"></a>IAMTimelineTransable:: TransAdd (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `TransAdd` método agrega una transición al objeto. Un objeto puede tener varias transiciones, pero no deben superponerse en el tiempo. Las transiciones deben estar dentro de los límites de tiempo del objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT TransAdd(
   IAMTimelineObj *pTrans
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTrans* 
</dt> <dd>

Puntero a la interfaz [**IAMTimelineObj**](iamtimelineobj.md) de la transición que se va a agregar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                                   | Descripción                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto.<br/>                                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | No se puede insertar la transición.<br/>              |
| <dl> <dt>**E \_ NOinterface**</dt> </dl> | *pTrans* no es un puntero a una transición.<br/> |



 

## <a name="remarks"></a>Observaciones

Si la transición se superpone a una transición existente, el método devuelve E \_ INVALIDARG.

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

[**Interfaz IAMTimelineTransable**](iamtimelinetransable.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




