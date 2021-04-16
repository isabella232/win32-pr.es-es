---
description: El método GetGroupCompressor recupera el filtro de compresión para el grupo especificado.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: 'ISmartRenderEngine:: GetGroupCompressor (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.GetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fd866daa225ab398e1a578aa8d21e73bad15e96d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680301"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a>ISmartRenderEngine:: GetGroupCompressor (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `GetGroupCompressor` método recupera el filtro de compresión para el grupo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetGroupCompressor(
   long        Group,
   IBaseFilter **pCompressor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Grupo* 
</dt> <dd>

Índice de base cero del grupo.

</dd> <dt>

*pCompressor* 
</dt> <dd>

Recibe un puntero a la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro de compresión. Recibe el valor **null** si no hay ningún filtro de compresión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Use este método para establecer las propiedades del filtro de compresión, como la velocidad de fotogramas clave. Llame a este método después de llamar a [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md), pero antes de representar el proyecto. A continuación, consulte el PIN de salida del filtro de compresión para la interfaz [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) , que contiene los métodos para establecer los parámetros de compresión. Suelte la interfaz cuando haya terminado. Si realiza cambios posteriores en la escala de tiempo, llame a **ConnectFrontEnd** y, a continuación, llame de nuevo a **GetGroupCompressor** para restablecer los parámetros de compresión.

En la devolución, si el valor de \* *pCompressor* no es **null**, la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarla.

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

[**Interfaz ISmartRenderEngine**](ismartrenderengine.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




