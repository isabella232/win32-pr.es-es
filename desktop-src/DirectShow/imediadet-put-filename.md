---
description: El método put \_ Filename especifica el nombre del archivo de origen que se usará en el detector de medios.
ms.assetid: 37bcc7ed-d2c1-4182-b85a-03bad92c5ba7
title: Método IMediaDet::p ut_Filename (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 542b84d3a1eec79b8408c7642bc08680fdc036ab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886841"
---
# <a name="imediadetput_filename-method"></a>Método IMediaDet::p ut \_ Filename

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `put_Filename` método especifica el nombre del archivo de origen que el detector de medios debe usar.

No llame a este método dos veces en el mismo objeto MediaDet. Para usar esta interfaz con más de un archivo de origen, cree instancias independientes del objeto MediaDet.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Filename(
  [in] BSTR newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ En\]
</dt> <dd>

Nombre de archivo del origen.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMediaDet (interfaz)**](imediadet.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




