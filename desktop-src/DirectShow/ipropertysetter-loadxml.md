---
description: El método LoadXML carga los datos de propiedad expresados en lenguaje de marcado extensible (XML).
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'IPropertySetter:: LoadXML (método) (QEDIT. h)'
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
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679117"
---
# <a name="ipropertysetterloadxml-method"></a>IPropertySetter:: LoadXML (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `LoadXML` método carga los datos de propiedad expresados en lenguaje de marcado extensible (XML).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PXML* \[ de\]
</dt> <dd>

Puntero a la interfaz **IUnknown** de un elemento XML creado por el analizador de Microsoft XML.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                                  | Descripción                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                      | No hay datos de propiedad.<br/>    |
| <dl> <dt>**S \_ correcto**</dt> </dl>                         | Correcto.<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                | Memoria insuficiente.<br/> |
| <dl> <dt>**\_formato de \_ archivo no válido de VFW E \_ \_**</dt> </dl> | Formato no válido.<br/>      |



 

## <a name="remarks"></a>Observaciones

Normalmente, las aplicaciones no tendrán que usar este método. DES lo usa internamente para cargar propiedades de archivos XTL.

Para usar este método, cree un objeto **IXMLDocument** y úselo para analizar un archivo XML. A continuación, use el objeto **IXMLDocument** para recuperar objetos **IXMLElement** . Si el objeto tiene propiedades, puede pasar el puntero **IXMLElement** al método **loadXML** . El método carga las propiedades en el establecedor de propiedad.

> [!Note]  
> Las interfaces **IXMLDocument** y **IXMLElement** se implementan en Microsoft XML Core Services (MSXML) versión 1,0, pero no se implementan en versiones más recientes de MSXML.

 

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

[**Interfaz IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




