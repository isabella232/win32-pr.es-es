---
description: El método GetStartStop recupera las horas de inicio y de detenerse del objeto, en relación con el elemento primario del objeto.
ms.assetid: de77e332-85ba-48bf-ae37-f198ce7c3a73
title: Método IAMTimelineObj::GetStartStop (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d808d7ac2ee3b6c1cbeddc39c730fc38b7032bde86ce726af03379d71241679c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118400791"
---
# <a name="iamtimelineobjgetstartstop-method"></a>IamTimelineObj::GetStartStop (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método recupera las horas de inicio y de detenerse del `GetStartStop` objeto, con respecto al elemento primario del objeto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStartStop(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pstart* 
</dt> <dd>

Recibe la hora de inicio, en unidades de 100 nanosegundos.

</dd> <dt>

*pStop* 
</dt> <dd>

Recibe la hora de detenerse, en unidades de 100 nanosegundos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Las composiciones, grupos y pistas siempre tienen una hora de inicio de 0.

Durante la representación, DES redondea las horas de inicio y de detenerse de un objeto al límite de marco más cercano. Sin embargo, DES no sobrescribe las horas del objeto. Si cambia la velocidad de fotogramas del grupo, las horas redondeadas siempre se calculan a partir de las horas originales. Para obtener más información, [consulte Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Para determinar las horas de inicio y de detenerse en el proyecto representado, pase los valores devueltos por al `GetStartStop` [**método IAMTimelineObj::FixTimes.**](iamtimelineobj-fixtimes.md)

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

[**IAMTimelineObj (interfaz)**](iamtimelineobj.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




