---
description: El método GetCountOfType recupera el número de objetos del tipo especificado que se encuentran en un grupo especificado y todos sus elementos secundarios.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: Método IAMTimeline::GetCountOfType (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetCountOfType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e9eb896f00752c5d9369cf494e7b1426347f82a7ebe2aac74f7822a936c2ffb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401066"
---
# <a name="iamtimelinegetcountoftype-method"></a>IamTimeline::GetCountOfType (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método recupera el número de objetos del tipo especificado que se encuentran en un grupo especificado y todos `GetCountOfType` sus elementos secundarios.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCountOfType(
   long                Group,
   long                *pVal,
   long                *pValWithComps,
   TIMELINE_MAJOR_TYPE MajorType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Grupo* 
</dt> <dd>

Número de índice del grupo para el que se va a recuperar el recuento.

</dd> <dt>

*pVal* 
</dt> <dd>

Recibe el número de objetos del tipo especificado incluido en el grupo y todas sus pistas virtuales, de forma recursiva.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Recibe el recuento devuelto en *pVal más* el número de composiciones buscadas, incluida esta.

</dd> <dt>

*MajorType* 
</dt> <dd>

Miembro del tipo [**enumerado \_ TIMELINE MAJOR \_ TYPE,**](timeline-major-type.md) especificando el tipo de objeto que se debe contar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT.**



| Código devuelto                                                                                  | Descripción                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Número de grupo no válido.<br/>      |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | **Argumento de** puntero NULL.<br/> |



 

## <a name="remarks"></a>Comentarios

Llamar a este método equivale a llamar a [**IAMTimelineComp::GetCountOfType**](iamtimelinecomp-getcountoftype.md) en el grupo especificado. Vea la sección Comentarios de ese método para obtener más información.

Normalmente, una aplicación no llamará a este método. El motor de representación lo llama internamente.

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

[**IAMTimeline (interfaz)**](iamtimeline.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




