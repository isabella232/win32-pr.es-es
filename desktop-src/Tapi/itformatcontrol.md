---
description: La interfaz ITFormatControl expone métodos que permiten a una aplicación recuperar información sobre el formato de una secuencia de recepción o transmisión para una llamada.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Interfaz ITFormatControl (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab42a9cacdf7986a652fff4e15195fec5f6b1aa319f06b631ee992541db40b82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406055"
---
# <a name="itformatcontrol-interface"></a>Interfaz ITFormatControl

\[Esta interfaz no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITFormatControl** expone métodos que permiten a una aplicación recuperar información sobre el formato de una secuencia de recepción o transmisión para una llamada.

El MSP de [H323](h323-msp.md) implementa esta interfaz y solo se expone cuando una llamada usa este proveedor de servicios.

## <a name="members"></a>Miembros

La **interfaz ITFormatControl** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITFormatControl también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITFormatControl** tiene estos métodos.



| Método                                                                     | Descripción                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetCurrentFormat**](itformatcontrol-getcurrentformat.md)               | Obtiene el formato multimedia de la secuencia actual.<br/>                        |
| [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) | Obtiene el número de funcionalidades asociadas al formato actual.<br/> |
| [**GetStreamCaps**](itformatcontrol-getstreamcaps.md)                     | Obtiene las funcionalidades asociadas a un índice de formato determinado.<br/>         |
| [**ReleaseFormat**](itformatcontrol-releaseformat.md)                     | Libera la estructura asociada al formato.<br/>                  |
| [**ReOrderCapabilities**](itformatcontrol-reordercapabilities.md)         | Establece un nuevo orden para las funcionalidades de formato.<br/>                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

