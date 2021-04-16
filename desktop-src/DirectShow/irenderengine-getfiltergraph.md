---
description: El método GetFilterGraph recupera el gráfico de filtro que el motor de representación ha construido, si existe.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: 'IRenderEngine:: GetFilterGraph (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c4750e6127c0d57758e46b2309f4d91afc110e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678943"
---
# <a name="irenderenginegetfiltergraph-method"></a>IRenderEngine:: GetFilterGraph (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetFilterGraph` método recupera el gráfico de filtro que el motor de representación ha construido, si existe.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppFG* \[ enuncia\]
</dt> <dd>

Recibe un puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del gráfico de filtro. Recibe el valor **null** si no hay ningún gráfico de filtros.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                                            | Descripción                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                   | Correcto.<br/>                            |
| <dl> <dt>**E \_ debe \_ inicializar el \_ representador**</dt> </dl> | No se pudo inicializar el motor de representación.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>              | Puntero no válido.<br/>                    |



 

## <a name="remarks"></a>Observaciones

Use el método [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para compilar el front-end del gráfico de filtro. Para la versión preliminar, use [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md) para completar el gráfico. Para la salida de archivos, conecte el front-end a una combinación de escritor de archivos/Mux. Para obtener más información, vea [representar un proyecto](rendering-a-project.md).

El gráfico resultante puede ejecutarse, pausarse, detenerse y buscarse; No obstante, no se puede cambiar la velocidad de reproducción.

En la devolución, si el valor de *\* ppFG* no es **null**, la interfaz **IGraphBuilder** tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando termine de usarla.

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

 

 




