---
description: El método SetCutPoint establece la hora a la que la transición corta de un origen al siguiente, si la transición se representa como un corte.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: 'IAMTimelineTrans:: SetCutPoint (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c1dad934d373a52b7e6c076c8c20dc8e1c6809ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690311"
---
# <a name="iamtimelinetranssetcutpoint-method"></a>IAMTimelineTrans:: SetCutPoint (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetCutPoint` método establece la hora a la que la transición corta de un origen al siguiente, si la transición se representa como un corte.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TLTime* 
</dt> <dd>

Punto de corte relativo al inicio de la transición, en unidades de 100-nanosegundos. Si el valor está fuera de los límites de la transición, se trunca a la hora válida más cercana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

De forma predeterminada, el punto de corte es el medio de la transición. Por ejemplo, en una transición que abarca un segundo, el punto de corte predeterminado es de 0,5 segundos en la transición.

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

[**Interfaz IAMTimelineTrans**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




