---
description: El método SetOutputBuffering especifica el número de fotogramas representados de antemano durante la versión preliminar.
ms.assetid: 6e69b196-a6ce-4ce0-8c48-58b1738fb197
title: Método IAMTimelineGroup::SetOutputBuffering (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputBuffering
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab249c1a6af63b0fc0f2ee535daeab1dec9cd558
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126892076"
---
# <a name="iamtimelinegroupsetoutputbuffering-method"></a>IamTimelineGroup::SetOutputBuffering (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetOutputBuffering` método especifica el número de fotogramas representados de antemano durante la versión preliminar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetOutputBuffering(
  [in] int nBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nBuffer* \[ En\]
</dt> <dd>

Número de fotogramas que se almacenarán en búfer durante la versión preliminar. Debe ser dos o más.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

Un búfer mayor requiere más memoria, pero puede dar lugar a una vista previa más fluida, especialmente durante los efectos o transiciones que requieren más tiempo para representarse. El búfer predeterminado es de 30 fotogramas.

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

[**IamTimelineGroup (interfaz)**](iamtimelinegroup.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




