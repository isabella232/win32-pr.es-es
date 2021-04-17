---
description: La interfaz IDxtAlphaSetter establece propiedades en el efecto del establecedor alfa. Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa el efecto del establecedor alfa.
ms.assetid: 9f0439b9-55d2-4526-ae4c-64ab90e11a64
title: Interfaz IDxtAlphaSetter (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtAlphaSetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0f4ad88d10f4a2538cddbdc31fa90bc5496bc7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680567"
---
# <a name="idxtalphasetter-interface"></a>Interfaz IDxtAlphaSetter

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IDxtAlphaSetter` interfaz establece las propiedades en el efecto del [establecedor alfa](alpha-setter-effect.md) .

Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa el efecto del establecedor alfa. Las aplicaciones DES no tienen que usar esta interfaz. Para establecer las propiedades de una transición en DES, use la interfaz [**IPropertySetter**](ipropertysetter.md) .

## <a name="members"></a>Miembros

La interfaz **IDxtAlphaSetter** hereda de **IDXEffect**. **IDxtAlphaSetter** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDxtAlphaSetter** tiene estos métodos.



| Método                                                  | Descripción                                                |
|:--------------------------------------------------------|:-----------------------------------------------------------|
| [**obtener \_ alfa**](idxtalphasetter-get-alpha.md)         | Recupera el valor alfa de toda la imagen.<br/> |
| [**obtener \_ AlphaRamp**](idxtalphasetter-get-alpharamp.md) | Recupera la propiedad de rampa alfa.<br/>              |
| [**poner \_ alfa**](idxtalphasetter-put-alpha.md)         | Especifica el valor alfa de la imagen completa.<br/> |
| [**Put \_ AlphaRamp**](idxtalphasetter-put-alpharamp.md) | Especifica la propiedad de rampa alfa.<br/>              |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El archivo de encabezado QEDIT. h no es compatible con los encabezados de Direct3D posteriores a la versión 7.

 

> [!Note]  
> Para obtener QEDIT. h, descargue la [actualización Microsoft Windows SDK para Windows Vista y .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). QEDIT. h no está disponible en el Microsoft Windows SDK para Windows 7 y .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>QEDIT. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 




