---
description: Sin implementar.
ms.assetid: f3be3b5a-7ab9-44ca-8a03-33fb905d3aea
title: 'IAMTimelineObj:: SetDirtyRange (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetDirtyRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8f0adee44de03560b347122a9c9cbdf500db897
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690728"
---
# <a name="iamtimelineobjsetdirtyrange-method"></a>IAMTimelineObj:: SetDirtyRange (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

Sin implementar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDirtyRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Iniciar* 
</dt> <dd>

Reservado.

</dd> <dt>

*Detención* 
</dt> <dd>

Reservado.

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

[**Interfaz IAMTimelineObj**](iamtimelineobj.md)
</dt> </dl>

 

 




