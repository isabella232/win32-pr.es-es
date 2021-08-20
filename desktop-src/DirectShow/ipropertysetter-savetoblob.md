---
description: El método SaveToBlob guarda los datos de propiedad en un formato de persistencia.
ms.assetid: 48201192-abda-484e-bdb3-442aca52b2bf
title: Método IPropertySetter::SaveToBlob (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SaveToBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c94cbb7b927e4bce7309e3e8a016b0e43bc6a0f9f3f319ee733e6e22132b47c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952553"
---
# <a name="ipropertysettersavetoblob-method"></a>IPropertySetter::SaveToBlob (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SaveToBlob` método guarda los datos de propiedad en un formato de persistencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SaveToBlob(
  [out] LONG *pcSize,
  [out] BYTE **ppb
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcSize* \[ out\]
</dt> <dd>

Recibe el tamaño de los datos, en bytes.

</dd> <dt>

*ppb* \[ out\]
</dt> <dd>

Recibe un puntero a una matriz de bytes que recibe los datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El método asigna memoria para la matriz de bytes. El autor de la llamada debe liberarlo mediante la **función CoTaskMemFree.**

Todos los nombres de propiedad y valores se truncan a 40 caracteres de longitud. Por esta razón, XML es el formato de persistencia preferido. Vea [**IXml2Dex (interfaz).**](ixml2dex.md)

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

[**IPropertySetter (interfaz)**](ipropertysetter.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




