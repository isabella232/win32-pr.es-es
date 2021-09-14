---
description: El método get \_ ReplicateX recupera el número de veces que el patrón de borrado se replica horizontalmente.
ms.assetid: 669a3bde-af8b-4d31-b914-41b71c95de1c
title: Método IDxtAsynceg::get_ReplicateX (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ReplicateX
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8855f819cb00d46297220c41deb6b81d6150e0f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061079"
---
# <a name="idxtjpegget_replicatex-method"></a>Método IDxtAsynceg::get \_ ReplicateX

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `get_ReplicateX` método recupera el número de veces que el patrón de borrado se replica horizontalmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_ReplicateX(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Recibe el número de veces que el patrón de borrado se replica horizontalmente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDxt Jpeg (interfaz)**](idxtjpeg.md)
</dt> </dl>

 

 




