---
description: El método SetDynamicReconnectLevel establece el nivel de reconexión dinámica durante la representación.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: Método IRenderEngine::SetDynamicReconnectLevel (Qedit.h)
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
ms.openlocfilehash: b43967753dd03d213a322ce569d113346542a57b5f37fd69fc28937198109049
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083685"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a>IRenderEngine::SetDynamicReconnectLevel (método)

> [!Note]  
> \[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

 

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

Combinación de [**marcas de reconexión dinámica,**](dynamic-reconnection-flags.md)especificando el nivel de reconexión dinámica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT:**



| Código devuelto                                                                               | Descripción                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto.<br/>         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Sin implementar.<br/> |



 

## <a name="remarks"></a>Comentarios

De forma predeterminada, el motor de representación básico carga todos los orígenes antes de representar un proyecto. Esto puede dar lugar a un tiempo de inicio largo. Con la reconexión dinámica, los orígenes solo se cargan cuando es necesario. Esto puede reducir el tiempo de inicio, pero posiblemente interferir con la reproducción fluida. Por lo general, entre más clips de origen use un proyecto, más podría beneficiarse de la reconexión dinámica.

El motor de representación inteligente no implementa este método.

> [!Note]  
> El archivo de encabezado Qedit.h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener Qedit.h, descargue la actualización del SDK de [Microsoft Windows para Windows Vista y .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit.h no está disponible en el SDK de Microsoft Windows para Windows 7 y .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRenderEngine (Interfaz)**](irenderengine.md)
</dt> <dt>

[Códigos de error y de éxito](error-and-success-codes.md)
</dt> </dl>

 

 




