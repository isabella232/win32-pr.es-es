---
description: Obtiene una nueva secuencia para el elemento especificado.
ms.assetid: fe25843c-2051-42fe-8737-eea39f6aeab9
title: 'IWiaTransferCallback:: GetNextStream (método) (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback.GetNextStream
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: fb2e92c9cade1dfd48efc3051b617997bf8473e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696519"
---
# <a name="iwiatransfercallbackgetnextstream-method"></a>IWiaTransferCallback:: GetNextStream (método)

Obtiene una nueva secuencia para el elemento especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetNextStream(
  [in]  LONG    lFlags,
  [in]  BSTR    bstrItemName,
  [in]  BSTR    bstrFullItemName,
  [out] IStream **ppDestination
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lFlags* \[ de\]
</dt> <dd>

Tipo: **Long**

Actualmente no se usa. Debe establecerse como cero.

</dd> <dt>

*bstrItemName* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre del elemento para el que se va a crear el flujo.

</dd> <dt>

*bstrFullItemName* \[ de\]
</dt> <dd>

Tipo: **BSTR**

Especifica el nombre completo del elemento para el que se va a crear el flujo.

</dd> <dt>

*ppDestination* \[ enuncia\]
</dt> <dd>

Tipo: **[IStream](/windows/win32/api/objidl/nn-objidl-istream)\*\***

Recibe la dirección de un puntero al nuevo objeto [IStream](/windows/win32/api/objidl/nn-objidl-istream) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Cuando este método se implementa mediante un filtro de procesamiento de imágenes, el minicontrolador de adquisición de imágenes de Windows (WIA) 2,0 lo llama durante la adquisición de la imagen para obtener la secuencia de destino del cliente.

**IWiaTransferCallback:: GetNextStream** de un filtro debe delegarse en el método de devolución de llamada de la aplicación. El filtro usa el flujo devuelto por la implementación de **IWiaTransferCallback:: GetNextStream** de la devolución de llamada de la aplicación para crear su propia secuencia que se devuelve al servicio WIA 2,0. El filtrado se realiza cuando el flujo del filtro llama al método [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) .

El flujo del filtro no puede realizar suposiciones sobre el número de bytes que se escriben en él en cada escritura, ya que los datos de la imagen sin filtrar pueden provienen del componente de vista previa de WIA 2,0 en lugar del controlador. El componente de vista previa de WIA 2,0 escribe siempre los datos de imagen sin filtrar completos en el flujo del filtro solo una vez, lo que significa que el flujo del filtro tiene un origen que escribe en él. Si el controlador y el componente de vista previa escriben en la secuencia del filtro, el flujo del filtro no puede suponer, por ejemplo, que recibirá el encabezado completo la primera vez que se llame a [IStream:: Write](/windows/win32/api/objidl/nf-objidl-isequentialstream-write) , aunque su controlador correspondiente siempre escribe primero los datos de encabezado en una sola escritura. Tampoco puede suponer que una escritura posterior contenga exactamente una línea de exploración. Por lo tanto, el flujo de filtrado puede tener que contar el número de bytes escritos en él para determinar, por ejemplo, dónde se inician los datos de la imagen.

La implementación **IWiaTransferCallback:: GetNextStream** del filtro de procesamiento de imágenes debe leer las propiedades necesarias para el procesamiento de imágenes del elemento para el que se adquiere la imagen. El filtro no lee las propiedades directamente desde el *pWiaItem2* pasado a [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md). En su lugar, el filtro debe llamar a [**FindItemByName**](-wia-iwiaitem2-finditembyname.md) en este elemento de WIA 2,0 para obtener el elemento de WIA 2,0 real. El motivo es que la imagen que se va a adquirir puede ser realmente un elemento secundario de *pWiaItem2*. Por ejemplo, durante una adquisición de carpeta, el filtro usa *pWiaItem2* para obtener los elementos secundarios de *pWiaItem2* en **IWiaTransferCallback:: GetNextStream** (durante una adquisición de carpeta, el controlador devuelve las imágenes representadas por los elementos secundarios de *pWiaItem2*). Lo mismo sucede cuando el componente WIA 2,0 Preview llama al filtro de procesamiento de imágenes que pasa un elemento secundario WIA 2,0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
