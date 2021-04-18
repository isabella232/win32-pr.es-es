---
description: El \_ método get FILENAME recupera el nombre del archivo de código fuente utilizado actualmente por el detector de medios.
ms.assetid: 68f0f1ea-74a2-4b65-9f1d-8699326d9d04
title: 'Método IMediaDet:: get_Filename (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.get_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 95a350dde3dfdc1c6046c8e31b8a2d9e62684788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680668"
---
# <a name="imediadetget_filename-method"></a>IMediaDet:: get \_ filename (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `get_Filename` método recupera el nombre del archivo de código fuente utilizado actualmente por el detector de medios.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Filename(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pval* \[ out, retval\]
</dt> <dd>

Recibe el nombre de archivo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

El método asigna memoria para la cadena. La aplicación debe llamar a **SysFreeString** para liberar memoria.

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

[**Interfaz IMediaDet**](imediadet.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




