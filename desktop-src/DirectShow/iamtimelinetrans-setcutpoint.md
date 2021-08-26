---
description: El método SetCutPoint establece la hora a la que la transición se reduce de un origen al siguiente, si la transición se representa como un corte.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: Método IAMTimelineTrans::SetCutPoint (Qedit.h)
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
ms.openlocfilehash: 2c411925ebe10ad35641e38ae2332605d7691ae24f0cc96ff716bd7d00e6603f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052075"
---
# <a name="iamtimelinetranssetcutpoint-method"></a>IamTimelineTrans::SetCutPoint (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método establece la hora a la que la transición se reduce de un origen al siguiente, si la transición `SetCutPoint` se representa como un corte.

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

Punto de corte relativo al inicio de la transición, en unidades de 100 nanosegundos. Si el valor queda fuera de los límites de la transición, se trunca al tiempo válido más cercano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

De forma predeterminada, el punto de corte es el centro de la transición. Por ejemplo, en una transición que abarca un segundo, el punto de corte predeterminado es 0,5 segundos en la transición.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IamTimelineTrans (interfaz)**](iamtimelinetrans.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




