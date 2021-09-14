---
description: El método put \_ Filter especifica un filtro de origen para el detector de medios que se usará.
ms.assetid: 59382cb0-c472-48b8-9cc5-52f9dbc61a07
title: Método IMediaDet::p ut_Filter (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd07ee3e2a18dcceae752e3923fd5fbdc88c0313
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886844"
---
# <a name="imediadetput_filter-method"></a>Método IMediaDet::p ut \_ Filter

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `put_Filter` método especifica un filtro de origen para el detector de medios que se usará.

> [!IMPORTANT]
> No agregue el filtro de origen a su propio gráfico de filtros ni use un filtro que ya esté en un gráfico de filtros. El objeto de detector de medios crea automáticamente un gráfico de filtro interno y colocar el filtro en otro gráfico puede provocar resultados inesperados.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Filter(
  [in] IUnknown *newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ En\]
</dt> <dd>

Puntero a la interfaz **IUnknown del filtro de** origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                                   | Descripción                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                             |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | *newVal* no apunta a un filtro.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | **Argumento de** puntero NULL.<br/>           |



 

## <a name="remarks"></a>Observaciones

Para la mayoría de las aplicaciones, es más sencillo llamar al método [**IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) con el nombre de un archivo de origen.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de Microsoft Windows para [Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMediaDet (interfaz)**](imediadet.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




