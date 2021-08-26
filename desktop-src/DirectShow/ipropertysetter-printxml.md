---
description: El método PrintXML convierte los datos de propiedad en una cadena XML.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: Método IPropertySetter::P rintXML (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5070a6906d7f30ab12171f551270f82b9851fa8c3990fade47aca6d2927509be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051515"
---
# <a name="ipropertysetterprintxml-method"></a>IPropertySetter::P rintXML (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `PrintXML` método convierte los datos de propiedad en una cadena XML.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszXML* \[ out\]
</dt> <dd>

Puntero a un búfer que recibe la cadena XML.

</dd> <dt>

*cbXML* \[ En\]
</dt> <dd>

Tamaño del búfer al que apunta *pszXML*, en bytes.

</dd> <dt>

*printPrinted* \[ out\]
</dt> <dd>

Puntero a una variable que recibe la longitud de la cadena XML. Puede ser **NULL.**

</dd> <dt>

*sangría* \[ En\]
</dt> <dd>

Número de niveles de sangría para la etiqueta más externa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente. De lo contrario, devuelve **un valor HRESULT** que indica la causa del error. Si la cadena XML es mayor que el búfer, el método devuelve E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

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

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




