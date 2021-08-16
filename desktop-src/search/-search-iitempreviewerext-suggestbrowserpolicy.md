---
description: Sugiere la directiva de seguridad que se va a aplicar al explorador.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: IItemPreviewerExt::SuggestBrowserPolicy (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IItemPreviewerExt.SuggestBrowserPolicy
api_type:
- COM
api_location: ''
ms.openlocfilehash: 84446b49ab723f161de8f148e95916202efe06176191e820ab8bafc88ed9158a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969764"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a>IItemPreviewerExt::SuggestBrowserPolicy (método)

Sugiere la directiva de seguridad que se va a aplicar al explorador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwContext* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Identificador de contexto de la operación. Invalide el valor predeterminado de *dwContext* para establecer el identificador de contexto en un valor de su elección.

</dd> <dt>

*pdwFlags* \[ out, retval\]
</dt> <dd>

Tipo: **DWORD \***

Puntero a un valor DWORD que contiene marcas de comprobación de comprobación. La **marca BROWSERPOLICY \_ UNTRUSTED \_ CONTENT** deshabilita cualquier posibilidad de que la versión preliminar pueda ejecutar script o ActiveX. El parámetro *pdwFlags* no debe ser un **puntero NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La [**interfaz IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede ser necesario usar la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) y las siguientes API: las interfaces [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) la estructura [**LINKINFO**](-search-linkinfo.md) y la [**enumeración LINKTYPE.**](-search-linktype.md)

Se recomienda encarecidamente usar la marca **\_ \_ BROWSERPOLICY UNTRUSTED CONTENT** para deshabilitar cualquier posibilidad de que la versión preliminar pueda ejecutar script o ActiveX. El **método IItemPreviewerExt::SuggestBrowserPolicy** puede devolver información sobre si el elemento en vista previa es de confianza o no. Esto permitirá que el control de tridente del elemento de vista previa ejecute el script e incluso ActiveX controles. Dado que el programa de vista previa suele usar archivos temporales para generar la versión preliminar, esto puede dar lugar a una ejecución inesperada de código y script en la zona Equipo local.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




