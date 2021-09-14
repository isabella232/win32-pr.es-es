---
description: Especifica un filtro de compresión que se usará al representar el grupo especificado.
ms.assetid: ba717cac-c5a8-4821-a5f0-dd9d5fe4834e
title: Método ISmartRenderEngine::SetGroupCompressor (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISmartRenderEngine.SetGroupCompressor
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9cb02a9d8daf7e6ba74a45299daa9d45ab63d5db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063235"
---
# <a name="ismartrenderenginesetgroupcompressor-method"></a>ISmartRenderEngine::SetGroupCompressor (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

Especifica un filtro de compresión que se usará al representar el grupo especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetGroupCompressor(
   long        Group,
   IBaseFilter *pCompressor
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

Puntero a la [**interfaz IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) del filtro de compresión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

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

[Códigos de error y correcto](error-and-success-codes.md)
</dt> </dl>

 

 




