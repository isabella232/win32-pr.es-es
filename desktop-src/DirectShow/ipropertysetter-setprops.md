---
description: El método SetProps establece las propiedades del objeto de destino en el estado adecuado durante el tiempo especificado.
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: Método IPropertySetter::SetProps (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a36b1735ea5b8261c37bee66ac90b9a186a55f0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160148"
---
# <a name="ipropertysettersetprops-method"></a>IPropertySetter::SetProps (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetProps` método establece las propiedades del objeto de destino en el estado adecuado durante el tiempo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTarget* \[ En\]
</dt> <dd>

Puntero al objeto de destino para el que se establecen las propiedades.

</dd> <dt>

*rtNow* \[ En\]
</dt> <dd>

Hora a la que se establecen las propiedades, en unidades de 100 nanosegundos, o –1 para establecer propiedades estáticas (aquellas que no varían con el tiempo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

DES llama a este método para establecer las propiedades en una transición o efecto. Normalmente, una aplicación no llamará a este método.

El objeto especificado por *pTarget* debe implementar la **interfaz IDispatch.**

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

[**IPropertySetter (interfaz)**](ipropertysetter.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




