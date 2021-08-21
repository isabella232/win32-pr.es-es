---
description: El método LoadXML carga los datos de propiedad expresados lenguaje de marcado extensible (XML).
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: Método IPropertySetter::LoadXML (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1779c6bcd37baad4bd423d0a46abd3741dd3a7939c1615a5871e6746729558c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952574"
---
# <a name="ipropertysetterloadxml-method"></a>IPropertySetter::LoadXML (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `LoadXML` método carga los datos de propiedad expresados lenguaje de marcado extensible (XML).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pxml* \[ En\]
</dt> <dd>

Puntero a la **interfaz IUnknown** de un elemento XML creado por el analizador XML de Microsoft.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                                  | Descripción                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | No hay datos de propiedad.<br/>    |
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Correcto.<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                | Memoria insuficiente.<br/> |
| <dl> <dt>**FORMATO DE ARCHIVO NO VÁLIDO VFW \_ E \_ \_ \_**</dt> </dl> | Formato no válido.<br/>      |



 

## <a name="remarks"></a>Comentarios

Normalmente, las aplicaciones no tendrán que usar este método. DES lo usa internamente para cargar propiedades desde archivos XTL.

Para usar este método, cree un **objeto IXMLDocument** y úselo para analizar un archivo XML. A continuación, **use el objeto IXMLDocument** para recuperar **objetos IXMLElement.** Si el objeto tiene propiedades, puede pasar el puntero **IXMLElement** al **método LoadXML.** El método carga las propiedades en el setter de propiedad.

> [!Note]  
> Las interfaces **IXMLDocument** e **IXMLElement** se implementan en Microsoft XML Core Services (MSXML) versión 1.0, pero no se implementan en versiones más recientes de MSXML.

 

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

 

 




