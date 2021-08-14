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
ms.openlocfilehash: 8208d886cd23dab797a9f89d3c050c9f46eff60c8cdd78c27c89dae7396c557a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397586"
---
# <a name="irenderenginegetfiltergraph-method"></a>IRenderEngine::GetFilterGraph (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

El método recupera el gráfico de filtro que ha construido el `GetFilterGraph` motor de representación, si lo hay.

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



 

## <a name="remarks"></a>Comentarios

Use el [**método IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) para compilar el front-end del gráfico de filtros. Para obtener una vista previa, [**use IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) para completar el gráfico. Para la salida del archivo, conecte el front-end a una combinación mux/escritor de archivos. Para obtener más información, vea [Representación de un Project](rendering-a-project.md).

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

[**IRenderEngine (Interfaz)**](irenderengine.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




