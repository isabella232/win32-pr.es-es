---
description: El método GetCountOfType recupera el número de objetos del tipo especificado que se encuentran en un grupo especificado y todos sus elementos secundarios.
ms.assetid: f3571fa5-8020-4079-ab7e-ba9ff280c0c5
title: 'IAMTimeline:: GetCountOfType (método) (QEDIT. h)'
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
ms.openlocfilehash: f0636eac7c651ed003c618e258f7dbf2bdd60996
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653514"
---
# <a name="iamtimelinegetcountoftype-method"></a>IAMTimeline:: GetCountOfType (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetCountOfType` método recupera el número de objetos del tipo especificado que se encuentran en un grupo especificado y todos sus elementos secundarios.

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

Recibe el número de objetos del tipo especificado contenidos en el grupo y todas sus pistas virtuales de forma recursiva.

</dd> <dt>

*pValWithComps* 
</dt> <dd>

Recibe el recuento devuelto en *pval* más el número de composiciones buscadas, incluido este.

</dd> <dt>

*MajorType* 
</dt> <dd>

Miembro del tipo [**\_ principal \_**](timeline-major-type.md) de la escala de tiempo, que especifica el tipo de objeto que se va a contar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** .



| Código devuelto                                                                                  | Descripción                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>                   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Número de grupo no válido.<br/>      |
| <dl> <dt>**\_puntero E**</dt> </dl>    | Argumento de puntero **nulo** .<br/> |



 

## <a name="remarks"></a>Observaciones

Llamar a este método equivale a llamar a [**IAMTimelineComp:: GetCountOfType**](iamtimelinecomp-getcountoftype.md) en el grupo especificado. Vea la sección Comentarios de ese método para obtener más información.

Normalmente, una aplicación no llamará a este método. Lo llama internamente el motor de representación.

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

[**Interfaz IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




