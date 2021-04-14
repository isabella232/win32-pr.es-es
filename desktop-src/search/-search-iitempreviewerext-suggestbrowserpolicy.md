---
description: Sugiere la Directiva de seguridad que se va a aplicar al explorador.
ms.assetid: 73541611-2024-4c33-ab03-e3204244c46c
title: 'IItemPreviewerExt:: SuggestBrowserPolicy (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497074"
---
# <a name="iitempreviewerextsuggestbrowserpolicy-method"></a>IItemPreviewerExt:: SuggestBrowserPolicy (método)

Sugiere la Directiva de seguridad que se va a aplicar al explorador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SuggestBrowserPolicy(
  [in]          DWORD dwContext,
  [out, retval] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwContext* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Identificador de contexto para la operación. Invalide el valor predeterminado de *dwContext* para establecer el identificador de contexto en un valor de su elección.

</dd> <dt>

*pdwFlags* \[ out, retval\]
</dt> <dd>

Tipo: **DWORD \** _

Un puntero a un valor DWORD que contiene marcas de comprobación de comprobación. La marca _ *BROWSERPOLICY de \_ \_ contenido* que no es de confianza * deshabilita cualquier posibilidad de que la vista previa pueda ejecutar script o ActiveX. El parámetro *pdwFlags* no debe ser un puntero **nulo** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admite en Windows XP y windows Server 2003, y ya no debe usarse.

Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) y las siguientes API: las interfaces [**ISearchProtocolUI**](-search-isearchprotocolui.md), [**IItemPropertyBag**](iitempropertybag.md) y [**ISearchItem**](-search-isearchitem.md) , la estructura [**LINKINFO**](-search-linkinfo.md) y la enumeración [**LINKTYPE**](-search-linktype.md) .

Se recomienda encarecidamente usar la marca de **\_ \_ contenido** que no es de confianza de BROWSERPOLICY para deshabilitar la posibilidad de que la vista previa pueda ejecutar script o ActiveX. El método **IItemPreviewerExt:: SuggestBrowserPolicy** puede devolver información sobre si el elemento que se está previsualizando es de confianza o no. Esto permitirá que el control Trident del controlador de vista previa ejecute un script e incluso controles ActiveX. Dado que el previsor suele usar archivos temporales para generar la vista previa, al hacerlo se puede producir un script y una ejecución de código inesperados en la zona de equipo local.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Redistribuible<br/>          | Búsqueda en el escritorio de Windows (WDS) 3,0<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IItemPreviewerExt**](-search-iitempreviewerext.md)
</dt> </dl>

 

 




