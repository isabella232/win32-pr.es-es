---
description: La interfaz ITFormatControl expone métodos que permiten a una aplicación recuperar información relacionada con el formato de una secuencia de recepción o transmisión para una llamada.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Interfaz ITFormatControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0735e7bfaf5222948cef5e047530a35cb19a125
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690831"
---
# <a name="itformatcontrol-interface"></a>Interfaz ITFormatControl

\[ Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITFormatControl** expone métodos que permiten a una aplicación recuperar información relacionada con el formato de una secuencia de recepción o transmisión para una llamada.

El [MSP de H323](h323-msp.md) implementa esta interfaz y solo se expone cuando una llamada utiliza este proveedor de servicios.

## <a name="members"></a>Miembros

La interfaz **ITFormatControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITFormatControl** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITFormatControl** tiene estos métodos.



| Método                                                                     | Descripción                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetCurrentFormat**](itformatcontrol-getcurrentformat.md)               | Obtiene el formato de medios de la secuencia actual.<br/>                        |
| [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) | Obtiene el número de funciones asociadas al formato actual.<br/> |
| [**GetStreamCaps**](itformatcontrol-getstreamcaps.md)                     | Obtiene las capacidades asociadas a un índice de formato determinado.<br/>         |
| [**ReleaseFormat**](itformatcontrol-releaseformat.md)                     | Libera la estructura asociada al formato.<br/>                  |
| [**ReOrderCapabilities**](itformatcontrol-reordercapabilities.md)         | Establece un nuevo orden para las capacidades de formato.<br/>                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                         |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

