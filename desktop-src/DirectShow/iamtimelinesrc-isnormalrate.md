---
description: El método IsNormalRate indica si el clip se reproducirá a la velocidad de reproducción normal; es decir, la velocidad de reproducción del archivo original.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: 'IAMTimelineSrc:: IsNormalRate (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.IsNormalRate
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e368efcf29d836cc23fa60ed34dae1a172978f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690939"
---
# <a name="iamtimelinesrcisnormalrate-method"></a>IAMTimelineSrc:: IsNormalRate (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `IsNormalRate` método indica si el clip se reproducirá con la velocidad de reproducción normal; es decir, la velocidad de reproducción del archivo original.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT IsNormalRate(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* 
</dt> <dd>

Recibe un valor booleano que indica cómo se representará el clip. Si el valor es **true**, el clip se reproducirá a la tarifa normal. De lo contrario, se reproducirá más rápido o más lento de lo normal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

La velocidad de reproducción de un clip viene determinada por las horas de inicio y detención del medio, en relación con las horas de la escala de tiempo:


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



Si esta relación es igual a 1, el clip se reproduce a la velocidad creada. De lo contrario, se reproducirá más rápido o más lento. Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IAMTimelineSrc**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




