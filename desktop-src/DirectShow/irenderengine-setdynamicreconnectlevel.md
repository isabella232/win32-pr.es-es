---
description: El método SetDynamicReconnectLevel establece el nivel de reconexión dinámica durante la representación.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'IRenderEngine:: SetDynamicReconnectLevel (método) (QEDIT. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae02fb6158b58cd5785aa7df539651acfbea5db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680713"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a>IRenderEngine:: SetDynamicReconnectLevel (método)

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

El `SetDynamicReconnectLevel` método establece el nivel de reconexión dinámica durante la representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Level* 
</dt> <dd>

Combinación de [**marcas de reconexión dinámica**](dynamic-reconnection-flags.md), que especifica el nivel de reconexión dinámica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** :



| Código devuelto                                                                               | Descripción                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | Correcto.<br/>         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Sin implementar.<br/> |



 

## <a name="remarks"></a>Observaciones

De forma predeterminada, el motor de representación básico carga todos los orígenes antes de representar un proyecto. Esto puede dar lugar a un tiempo de inicio largo. Con la reconexión dinámica, los orígenes se cargan solo cuando sea necesario. Esto puede acortar el tiempo de inicio, pero podría interferir con la reproducción fluida. Por lo general, cuanto más clips de origen usa un proyecto, más se puede beneficiar de la reconexión dinámica.

El motor de representación inteligente no implementa este método.

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

 

 




