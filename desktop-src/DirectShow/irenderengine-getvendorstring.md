---
description: El método GetVendorString recupera el nombre del proveedor. En el caso de los objetos del motor de representación que se proporcionan en DirectShow, la cadena del proveedor es &\# 0034; Microsoft Corporation&\# 0034;.
ms.assetid: d0a4c525-67dc-419a-b4d6-8cd51888fd8a
title: 'IRenderEngine:: GetVendorString (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetVendorString
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abf339b73fa058c6554965c16428774ad1fdd32c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680718"
---
# <a name="irenderenginegetvendorstring-method"></a>IRenderEngine:: GetVendorString (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetVendorString` método recupera el nombre del proveedor. En el caso de los objetos del motor de representación que se proporcionan en DirectShow, la cadena del proveedor es "Microsoft Corporation".

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVendorString(
  [out, retval] BSTR *pVendorID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVendorID* \[ out, retval\]
</dt> <dd>

Recibe un **BSTR** que contiene la cadena del proveedor.

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

[**Interfaz IRenderEngine**](irenderengine.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




