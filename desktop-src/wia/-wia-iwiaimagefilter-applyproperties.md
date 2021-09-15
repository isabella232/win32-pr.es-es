---
description: Permite que el filtro de procesamiento de imágenes vuelva a escribir propiedades en el controlador (y el dispositivo).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: Método IWiaImageFilter::ApplyProperties (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter.ApplyProperties
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3c20527ee587b975adea34e7c480349836620015
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572292"
---
# <a name="iwiaimagefilterapplyproperties-method"></a>IWiaImageFilter::ApplyProperties (método)

Permite que el filtro de procesamiento de imágenes vuelva a escribir propiedades en el controlador (y el dispositivo).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWiaPropertyStorage* \[ En\]
</dt> <dd>

Tipo: **[ **IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)\***

Especifica un puntero a [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para las propiedades que se aplicarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

No llame a este método directamente desde la aplicación. Se llama mediante Windows Adquisición de imágenes (WIA) 2.0 después de que el filtro de procesamiento de imágenes haya procesado los datos sin procesar.

*pWiaPropertyStorage es* la [**interfaz IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) en la que el filtro de procesamiento de imágenes debe escribir propiedades. Un filtro de procesamiento de imágenes solo debe usar [el método IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) para escribir propiedades.

Este método permite que el filtro de procesamiento de imágenes vuelva a escribir propiedades en el controlador (y el dispositivo). Esto puede ser necesario para los filtros que implementan características como la exposición automática durante el examen de películas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
