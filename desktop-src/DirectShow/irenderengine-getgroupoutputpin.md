---
description: El método GetGroupOutputPin recupera el PIN de salida para el grupo especificado.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'IRenderEngine:: GetGroupOutputPin (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680615"
---
# <a name="irenderenginegetgroupoutputpin-method"></a>IRenderEngine:: GetGroupOutputPin (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetGroupOutputPin` método recupera el PIN de salida para el grupo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Grupo* 
</dt> <dd>

Índice de base cero que especifica el grupo.

</dd> <dt>

*ppRenderPin* \[ enuncia\]
</dt> <dd>

Recibe un puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del terminal de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles figuran los siguientes:



| Código devuelto                                                                                                  | Descripción                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                      | El grupo no tiene un PIN de salida.<br/>                              |
| <dl> <dt>**S \_ correcto**</dt> </dl>                         | Correcto.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argumento no válido.<br/>                                               |
| <dl> <dt>**E \_ debe \_ inicializar el \_ representador**</dt> </dl>       | No se pudo inicializar el motor de representación.<br/>                             |
| <dl> <dt>**\_puntero E**</dt> </dl>                    | Puntero no válido.<br/>                                                |
| <dl> <dt>**el \_ motor de representación E \_ \_ está \_ roto**</dt> </dl> | No se pudo realizar la operación porque el proyecto no se representó correctamente.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>                 | error inesperado.<br/>                                               |



 

## <a name="remarks"></a>Observaciones

Antes de llamar a este método, llame a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para compilar el front-end del gráfico. Cada grupo representa un flujo multimedia único y el front-end tiene un PIN de salida correspondiente.

Puede usar este método para crear la parte de representación de un gráfico de escritura de archivos. Conecte los pin de salida a filtros de multiplexor y filtros de escritura de archivo. Para obtener más información, vea [representar un proyecto](rendering-a-project.md).

En la vista previa, no es necesario llamar a este método. Simplemente llame a **ConnectFrontEnd** seguido de [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md).

Si el método devuelve S \_ correcto, la interfaz **IPin** que devuelve tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando termine de usarla.

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

 

 




