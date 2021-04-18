---
description: Función de proxy para el método GetAuthor.
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: IWICComponentInfo_GetAuthor_Proxy función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f181a567ae4089870d324c7a7e0d67a34b965b5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707002"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a>IWICComponentInfo \_ GetAuthor \_ función proxy

Función de proxy para el método [**GetAuthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Este \_ PTR* \[ en\]
</dt> <dd>

Tipo: **[**IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _

Puntero a este objeto [_ *IWICComponentInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) .

</dd> <dt>

*cchAuthor* \[ de\]
</dt> <dd>

Tipo: **uint**

Tamaño del búfer de *wzAuthor* .

</dd> <dt>

*wzAuthor* \[ in, out\]
</dt> <dd>

Tipo: **WCHAR \** _

Puntero que recibe el nombre del autor del componente.

La cadena devuelta es específica de la configuración regional, 1033 de forma predeterminada.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Tipo: **uint \** _

Puntero que recibe la longitud real del nombre de los autores del componente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP con SP2, \[ solo aplicaciones de escritorio de Windows Vista\]<br/>                                                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                                                                             |
| Archivo DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




