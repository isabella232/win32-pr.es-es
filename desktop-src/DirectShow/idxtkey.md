---
description: La interfaz IDxtKey establece propiedades en la transición de clave. Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa la transición de la clave.
ms.assetid: b929bf0c-8aaf-456e-b692-e23d88e480dd
title: Interfaz IDxtKey (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f4f1bc6a5dd0e89789e098fc4180bfc826f10c93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680302"
---
# <a name="idxtkey-interface"></a>Interfaz IDxtKey

> [!Note]  
> \[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

 

La `IDxtKey` interfaz establece las propiedades de la transición de [clave](key-transition.md) .

Esta interfaz la usan internamente los servicios de edición de DirectShow (DES) cuando representa la transición de la clave. Las aplicaciones DES no necesitan usar esta interfaz. Para establecer las propiedades de una transición en DES, use la interfaz [**IPropertySetter**](ipropertysetter.md) .

## <a name="members"></a>Miembros

La interfaz **IDxtKey** hereda de **IDXEffect**. **IDxtKey** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IDxtKey** tiene estos métodos.



| Método                                            | Descripción                                                                            |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**obtener \_ matiz**](idxtkey-get-hue.md)               | Recupera el valor de matiz en el que se va a hacer la tecla.<br/>                                    |
| [**obtener \_ invertir**](idxtkey-get-invert.md)         | Recupera un valor booleano que indica si se invierte la operación de clave.<br/> |
| [**obtener \_ KeyType**](idxtkey-get-keytype.md)       | Recupera el tipo de clave.<br/>                                                  |
| [**obtención de \_ luminancia**](idxtkey-get-luminance.md)   | Recupera el valor de luminancia en el que se va a hacer la tecla.<br/>                              |
| [**obtener \_ RGB**](idxtkey-get-rgb.md)               | Recupera el color RGB en el que se va a hacer la tecla.<br/>                                    |
| [**obtener \_ similitud**](idxtkey-get-similarity.md) | Recupera el intervalo de datos de color que se vuelve transparente.<br/>                 |
| [**poner \_ matiz**](idxtkey-put-hue.md)               | Especifica el valor de matiz en el que se va a hacer la tecla.<br/>                                    |
| [**poner \_ invertir**](idxtkey-put-invert.md)         | Especifica si se invierte la operación de clave.<br/>                            |
| [**poner \_ KeyType**](idxtkey-put-keytype.md)       | Especifica el tipo de clave.<br/>                                                  |
| [**poner \_ luminancia**](idxtkey-put-luminance.md)   | Especifica el valor de luminancia en el que se va a hacer la tecla.<br/>                              |
| [**colocar \_ RGB**](idxtkey-put-rgb.md)               | Especifica el color RGB en el que se va a hacer la tecla.<br/>                                    |
| [**similitud de put \_**](idxtkey-put-similarity.md) | Especifica el intervalo de datos de color que se vuelve transparente.<br/>                 |



 

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



 

 




