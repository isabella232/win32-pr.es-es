---
description: Sugiere que la directiva de seguridad se aplique al explorador.
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
ms.openlocfilehash: 0a4f248edbfa4a1779016e40d73051d8c1d9acac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574584"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a>IItemPreviewerExt::SuggestBrowserPolicy (método)

Sugiere que la directiva de seguridad se aplique al explorador.

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

Identificador de contexto de la operación. Invalide el valor predeterminado de *dwContext* para establecer el identificador de contexto en el valor que elija.

</dd> <dt>

*pdwFlags* \[ out, retval\]
</dt> <dd>

Tipo: **DWORD \***

Puntero a un valor DWORD que contiene marcas de comprobación de comprobación. La **marca BROWSERPOLICY \_ UNTRUSTED \_ CONTENT** deshabilita cualquier posibilidad de que la versión preliminar pueda ejecutar script o ActiveX. El parámetro *pdwFlags* no debe ser un **puntero NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

La [**interfaz IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admite en Windows XP y Windows Server 2003 y ya no se debe usar.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) y las siguientes API: las interfaces [**ISearchProtocolUI,**](-search-isearchprotocolui.md) [**IItemPropertyBag**](iitempropertybag.md) e [**ISearchItem,**](-search-isearchitem.md) la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE.**](-search-linktype.md)

Se recomienda encarecidamente usar la marca **BROWSERPOLICY \_ UNTRUSTED \_ CONTENT** para deshabilitar cualquier posibilidad de que la versión preliminar pueda ejecutar script o ActiveX. El **método IItemPreviewerExt::SuggestBrowserPolicy** puede devolver información sobre si el elemento que se está visualizando es de confianza o no. Esto permitirá que el control tridente del control de vista previa ejecute el script e incluso ActiveX controles. Dado que el programa de vista previa suele usar archivos temporales para generar la vista previa, esto puede dar lugar a una ejecución inesperada de código y script en la zona Equipo local.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de escritorio de SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Windows Búsqueda de escritorio (WDS) 3.0<br/>          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




