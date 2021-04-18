---
title: Interfaz IWMPError (VB y C) (WMP. h)
description: Proporciona propiedades y métodos para tener acceso a una colección de interfaces IWMPErrorItem para recuperar información de error. La interfaz IWMPError expone las siguientes propiedades.
ms.assetid: c7d9f834-43ed-40a2-95a3-b1633f025118
keywords:
- IWMPError (VB y C) interfaz de Windows Media Player
- IWMPError (VB y C) interfaz de Windows Media Player, se describe
topic_type:
- apiref
api_name:
- IWMPError (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289a39093c38e7a4b0cc43cb8f318e321ae8ef53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690422"
---
# <a name="iwmperror-vb-and-c-interface"></a>Interfaz IWMPError (VB y C#)

Proporciona propiedades y métodos para tener acceso a una colección de interfaces **IWMPErrorItem** para recuperar información de error.

La interfaz **IWMPError** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La interfaz **IWMPError (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IWMPError (VB y C#)** tiene estos métodos.



| Método                                                                         | Descripción                                                                                                                                   |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**clearErrorQueue**](wmplibiwmperror-iwmperror-clearerrorqueue--vb-and-c.md) | Borra los errores de la cola de errores.<br/>                                                                                            |
| [**WebHelp**](wmplibiwmperror-iwmperror-webhelp--vb-and-c.md)                 | Inicia la página de ayuda Web de Microsoft Windows Media Player para mostrar información adicional sobre el primer error en la cola de errores.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IWMPError (VB y C#)** tiene estas propiedades.



| Propiedad                                                                        | Tipo de acceso           | Descripción                                                                                                                         |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**errorCount**](wmplibiwmperror-iwmperror-errorcount--vb-and-c.md)<br/> | Solo lectura<br/>  | Obtiene el número de errores en la cola de errores.<br/>                                                                            |
| [**Elemento**](iwmperror-item--vb-and-c.md)<br/>                             | Lectura/escritura<br/> | Obtiene una interfaz **IWMPErrorItem** en el índice especificado de la cola de errores. En C#, este es el método **Get \_ Item** .<br/> |



 

Obtenga una interfaz **IWMPError** con la siguiente propiedad.



| Object                                                                   | Propiedad                                                       |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Error**](axwmplib-axwindowsmediaplayer-error--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPErrorItem (VB y C#)**](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





