---
description: Obtiene el elemento de búsqueda de los datos especificados. Se llama a este método una vez para cada dirección URL procesada por el recopilador y recupera un puntero al objeto ISearchItem.
ms.assetid: 35893bc9-8327-44f9-a9fc-7855c5c063e3
title: ISearchProtocolUI::GetSearchItemForUrl (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchProtocolUI.GetSearchItemForUrl
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8636f42026fe44131e149b0e378089b70c7d4f49b9e23b5d48ebe50aa5721d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119594815"
---
# <a name="isearchprotocoluigetsearchitemforurl-method"></a>ISearchProtocolUI::GetSearchItemForUrl (método)

Obtiene el elemento de búsqueda de los datos especificados. Se llama a este método una vez para cada dirección URL procesada por el recopilador y recupera un puntero al [**objeto ISearchItem.**](-search-isearchitem.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetSearchItemForUrl(
  [in]          LPCOLESTR        pcwszURL,
  [in]          IItemPropertyBag *pPropertyBag,
  [out, retval] ISearchItem      **ppSearchItem
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pcwszURL* \[ En\]
</dt> <dd>

Tipo: **LPCOLESTR**

Puntero a una cadena Unicode terminada en datos NULL que contiene el elemento de búsqueda de la dirección URL a la que se tiene acceso.

</dd> <dt>

*pPropertyBag* \[ En\]
</dt> <dd>

Tipo: **IItemPropertyBag \***

Puntero a un [**objeto IItemPropertyBag**](iitempropertybag.md) que contiene información sobre el elemento de búsqueda, incluidas las propiedades del elemento.

</dd> <dt>

*ppSearchItem* \[ out, retval\]
</dt> <dd>

Tipo: **[ **ISearchItem**](-search-isearchitem.md)\*\***

Recibe la dirección de un puntero al [**objeto ISearchItem**](-search-isearchitem.md) creado por este método. Este objeto contiene información sobre el elemento de búsqueda, como el nombre de archivo del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

El **método ISearchProtocolUI::GetSearchItemForUrl** solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede ser necesario usar la interfaz [**ISearchProtocolUI**](-search-isearchprotocolui.md) y las SIGUIENTES API: las interfaces [**IItemPreviewerExt,**](-search-iitempreviewerext.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE.**](-search-linktype.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISearchProtocolUI**](-search-isearchprotocolui.md)
</dt> </dl>

 

 




