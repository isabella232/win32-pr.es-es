---
description: El método GetFilterGraph recupera el gráfico de filtro que ha construido el motor de representación, si lo hay.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: Método IRenderEngine::GetFilterGraph (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160136"
---
# <a name="irenderenginegetfiltergraph-method"></a>IRenderEngine::GetFilterGraph (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método recupera el gráfico de filtro que ha construido el motor de `GetFilterGraph` representación, si lo hay.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppFG* \[ out\]
</dt> <dd>

Recibe un puntero a la interfaz [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del gráfico de filtros. Recibe el valor **NULL si** no hay ningún gráfico de filtro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                                            | Descripción                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Correcto.<br/>                            |
| <dl> <dt>**E \_ MUST \_ INIT \_ RENDERER**</dt> </dl> | No se pudo inicializar el motor de representación.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>              | Puntero no válido.<br/>                    |



 

## <a name="remarks"></a>Observaciones

Use el [**método IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) para compilar el front-end del gráfico de filtro. Para obtener una vista previa, [**use IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) para completar el gráfico. Para la salida del archivo, conecte el front-end a una combinación de mux/escritor de archivos. Para obtener más información, vea [Representación de un Project](rendering-a-project.md).

El gráfico resultante se puede ejecutar, pausar, detener y buscar; Sin embargo, no se puede cambiar la velocidad de reproducción.

En la devolución, si el valor de *\* ppFG* no es **NULL,** la **interfaz IGraphBuilder** tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

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

 

 




