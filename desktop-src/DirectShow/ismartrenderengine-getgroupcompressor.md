---
description: El método GetGroupCompressor recupera el filtro de compresión para el grupo especificado.
ms.assetid: 9d71e659-7abb-48c6-b9bd-5239560dc150
title: Método ISmartRenderEngine::GetGroupCompressor (Qedit.h)
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
ms.openlocfilehash: 65915039d26b3c8739441240419e61e0cbacf5a6f4212cbb1c8b456f55dfcbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817443"
---
# <a name="ismartrenderenginegetgroupcompressor-method"></a>ISmartRenderEngine::GetGroupCompressor (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

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

Recibe un puntero a la [**interfaz IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro de compresión. Recibe el valor **NULL si** no hay ningún filtro de compresión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Comentarios

Use este método para establecer propiedades en el filtro de compresión, como la velocidad de fotogramas clave. Llame a este método después de llamar [**a IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md), pero antes de representar el proyecto. A continuación, consulte el pin de salida del filtro de compresión para la [**interfaz IAMVideoCompression,**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression) que contiene métodos para establecer parámetros de compresión. Libere la interfaz cuando haya terminado. Si realiza cambios posteriores en la escala de tiempo, llame a **ConnectFrontEnd** y vuelva a llamar a **GetGroupCompressor** para restablecer los parámetros de compresión.

En la devolución, si el valor de \* *pCompressor* no es **NULL,** la interfaz [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) tiene un recuento de referencias pendiente. Asegúrese de liberar la interfaz cuando haya terminado de usarlo.

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

[**ISmartRenderEngine (interfaz)**](ismartrenderengine.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




