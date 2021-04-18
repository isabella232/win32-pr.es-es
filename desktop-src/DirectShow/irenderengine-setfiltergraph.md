---
description: El método SetFilterGraph especifica un gráfico de filtro para que lo use el motor de representación.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'IRenderEngine:: SetFilterGraph (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681222"
---
# <a name="irenderenginesetfiltergraph-method"></a>IRenderEngine:: SetFilterGraph (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetFilterGraph` método especifica un gráfico de filtro para que lo use el motor de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFG* 
</dt> <dd>

Puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del gráfico de filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                                            | Descripción                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Correcto.<br/>                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Argumento no válido.<br/>                   |
| <dl> <dt>**E \_ debe \_ inicializar el \_ representador**</dt> </dl> | No se pudo inicializar el motor de representación.<br/> |



 

## <a name="remarks"></a>Observaciones

La mayoría de las aplicaciones no necesitan llamar a este método. Es más habitual permitir que el motor de representación cree el gráfico automáticamente, llamando al método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) .

Este método produce un error si el motor de representación ya tiene un gráfico de filtro.

No recupere nunca un puntero a un gráfico de filtro creado por un motor de representación y, a continuación, úselo como parámetro para este método en otro motor de representación. Si lo hace, se producirán resultados imprevisibles.

El método **ConnectFrontEnd** anula el gráfico de filtros existente, pero mantiene la misma instancia de Filter Graph Manager.

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

[**Interfaz IRenderEngine**](irenderengine.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




