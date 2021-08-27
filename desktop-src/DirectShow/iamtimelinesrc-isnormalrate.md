---
description: El método IsNormalRate indica si el clip se reproducirá a la velocidad de reproducción normal; es decir, la velocidad de reproducción del archivo original.
ms.assetid: 4a8fe415-f9eb-450d-9a75-e528577050d9
title: Método IAMTimelineSrc::IsNormalRate (Qedit.h)
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
ms.openlocfilehash: 4d1c0b355b0eedee29dafb92debbabac5c7b3e574d2f161827626bc73f72c035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083875"
---
# <a name="iamtimelinesrcisnormalrate-method"></a>IamTimelineSrc::IsNormalRate (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método indica si el clip se reproducirá a la velocidad de reproducción normal; es decir, la velocidad `IsNormalRate` de reproducción del archivo original.

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

Recibe un valor booleano que indica cómo se representará el clip. Si el valor es **TRUE,** el clip se reproducirá a la velocidad normal. De lo contrario, se reproducirá más rápido o más lento de lo normal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

La velocidad de reproducción de un clip viene determinada por las horas de inicio y de detenerse de los medios, en relación con sus horas de escala de tiempo:


```C++
Playback rate = (Media Stop <entity type="mdash"/> Media Start) / (Timeline Stop <entity type="mdash"/> Timeline Start)
```



Si esta proporción es igual a 1, el clip se reproduce a la velocidad de creación. De lo contrario, se reproduce más rápido o más lento. Para obtener más información, vea [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IamTimelineSrc (interfaz)**](iamtimelinesrc.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




