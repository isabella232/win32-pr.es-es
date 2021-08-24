---
title: Interfaz IWMPError (VB y C) (Wmp.h)
description: Proporciona propiedades y métodos para acceder a una colección de interfaces IWMPErrorItem para recuperar información de error. La interfaz IWMPError expone las siguientes propiedades.
ms.assetid: c7d9f834-43ed-40a2-95a3-b1633f025118
keywords:
- Interfaz IWMPError (VB y C) Reproductor de Windows Media
- Interfaz IWMPError (VB y C) Reproductor de Windows Media , descrito
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
ms.openlocfilehash: 5f3ff7635e423d70447e371d61fbbadf02aa14c2476e118be79cbb25d974348b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736185"
---
# <a name="iwmperror-vb-and-c-interface"></a>Interfaz IWMPError (VB y C#)

Proporciona propiedades y métodos para acceder a una colección de interfaces **IWMPErrorItem** para recuperar información de error.

La **interfaz IWMPError** expone las siguientes propiedades.

## <a name="members"></a>Miembros

La **interfaz IWMPError (VB y C#)** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IWMPError (VB y C#)** tiene estos métodos.



| Método                                                                         | Descripción                                                                                                                                   |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**clearErrorQueue**](wmplibiwmperror-iwmperror-clearerrorqueue--vb-and-c.md) | Borra los errores de la cola de errores.<br/>                                                                                            |
| [**Webhelp**](wmplibiwmperror-iwmperror-webhelp--vb-and-c.md)                 | Inicia la página microsoft Reproductor de Windows Media Web Help para mostrar más información sobre el primer error en la cola de errores.<br/> |



 

### <a name="properties"></a>Propiedades

La **interfaz IWMPError (VB y C#)** tiene estas propiedades.



| Propiedad                                                                        | Tipo de acceso           | Descripción                                                                                                                         |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**errorCount**](wmplibiwmperror-iwmperror-errorcount--vb-and-c.md)<br/> | Solo lectura<br/>  | Obtiene el número de errores de la cola de errores.<br/>                                                                            |
| [**Elemento**](iwmperror-item--vb-and-c.md)<br/>                             | Lectura/escritura<br/> | Obtiene una **interfaz IWMPErrorItem** en el índice especificado de la cola de errores. En C#, este es el **método get \_ Item.**<br/> |



 

Obtenga una **interfaz IWMPError** mediante la siguiente propiedad.



| Object                                                                   | Propiedad                                                       |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [Objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) | [**Error**](axwmplib-axwindowsmediaplayer-error--vb-and-c.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Wmp.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces para Visual Basic .NET y C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interfaz IWMPErrorItem (VB y C#)**](iwmperroritem--vb-and-c.md)
</dt> </dl>

 

 





