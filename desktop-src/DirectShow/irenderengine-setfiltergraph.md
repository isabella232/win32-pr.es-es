---
description: El método SetFilterGraph especifica un gráfico de filtro para que lo use el motor de representación.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: Método IRenderEngine::SetFilterGraph (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126886700"
---
# <a name="irenderenginesetfiltergraph-method"></a>IRenderEngine::SetFilterGraph (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El `SetFilterGraph` método especifica un gráfico de filtro para el motor de representación que se usará.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pfg* 
</dt> <dd>

Puntero a la [**interfaz IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del gráfico de filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                            | Descripción                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Correcto.<br/>                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Argumento no válido.<br/>                   |
| <dl> <dt>**E \_ MUST \_ INIT \_ RENDERER**</dt> </dl> | No se pudo inicializar el motor de representación.<br/> |



 

## <a name="remarks"></a>Observaciones

La mayoría de las aplicaciones no necesitan llamar a este método. Es más habitual dejar que el motor de representación compile el gráfico automáticamente mediante una llamada al [**método IRenderEngine::ConnectFrontEnd.**](irenderengine-connectfrontend.md)

Se produce un error en este método si el motor de representación ya tiene un gráfico de filtros.

Nunca recupere un puntero a un gráfico de filtro creado por un motor de representación y, a continuación, úselo como parámetro para este método en otro motor de representación. Si lo hace, se producirán resultados imprevisibles.

El **método ConnectFrontEnd** desmonta cualquier gráfico de filtros existente, pero mantiene la misma instancia de Filter Graph Manager.

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

[**IRenderEngine (interfaz)**](irenderengine.md)
</dt> <dt>

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




