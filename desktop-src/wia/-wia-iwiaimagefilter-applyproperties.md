---
description: Permite que el filtro de procesamiento de imágenes escriba las propiedades de nuevo en el controlador (y en el dispositivo).
ms.assetid: b9bb8d81-2945-46ba-a0a2-7009000574aa
title: 'IWiaImageFilter:: ApplyProperties (método) (WIA. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716050"
---
# <a name="iwiaimagefilterapplyproperties-method"></a>IWiaImageFilter:: ApplyProperties (método)

Permite que el filtro de procesamiento de imágenes escriba las propiedades de nuevo en el controlador (y en el dispositivo).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ApplyProperties(
  [in] IWiaPropertyStorage *pWiaPropertyStorage
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWiaPropertyStorage* \[ de\]
</dt> <dd>

Tipo: **[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) \** _

Especifica un puntero a [_ *IWiaPropertyStorage* *](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) para las propiedades que se van a aplicar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

No llame a este método directamente desde su aplicación. Lo llama la adquisición de imágenes de Windows (WIA) 2,0 después de que el filtro de procesamiento de imágenes haya procesado los datos sin procesar.

*pWiaPropertyStorage* es la interfaz de [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) en la que el filtro de procesamiento de imágenes debe escribir propiedades. Un filtro de procesamiento de imágenes solo debe usar el método [IPropertyStorage:: WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) para escribir propiedades.

Este método permite que el filtro de procesamiento de imágenes escriba las propiedades de nuevo en el controlador (y en el dispositivo). Esto puede ser necesario para los filtros que implementan características como la exposición automática durante el análisis de la película.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
