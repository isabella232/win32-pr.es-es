---
title: Valores devueltos (características de accesibilidad de Windows)
description: En este tema se describen los valores devueltos más comunes y otros valores devueltos que se pueden ver con menos frecuencia.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae2ccaf8bc74b1802be7569bc9e783cde4e11f9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488663"
---
# <a name="return-values-windows-accessibility-features"></a>Valores devueltos (características de accesibilidad de Windows)

En este tema se describen los valores devueltos más comunes y otros valores devueltos que se pueden ver con menos frecuencia.

## <a name="common-return-values"></a>Valores devueltos comunes

Los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) devuelven uno de los valores siguientes, definidos en Winerror. h u otro código de error del modelo de objetos componentes (com) estándar:



|                         |                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ correcto                   | El método se ha llevado a cabo de forma correcta.                                                                                                                                                                                                                                                                                                                                                                     |
| S \_ false                | El método se realizó correctamente en parte. Esto sucede cuando el método se ejecuta correctamente, pero la información solicitada no está disponible. Por ejemplo, Microsoft Active Accessibility devuelve S \_ false si se llama a [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) para recuperar un objeto secundario en un punto determinado y el punto especificado no está dentro del objeto o del elemento secundario del objeto. |
| DISP \_ E \_ MEMBERNOTFOUND | El objeto no admite la propiedad o acción solicitada. Por ejemplo, un botón de reenvío devuelve este valor si se solicita su [propiedad Value](value-property.md), ya que no tiene una propiedad Value.                                                                                                                                                                           |
| E \_ NOTIMPL              | El método no está implementado. Este valor se produce cuando un cliente llama a un método que todavía no se admite en ese sistema operativo.                                                                                                                                                                                                                                                         |
| E \_ INVALIDARG           | Uno o varios argumentos no son válidos. Este error se produce cuando el llamador intenta identificar un objeto secundario mediante un identificador que el servidor no reconoce. Este error también se produce cuando un cliente intenta identificar un objeto secundario dentro de un objeto que no tiene elementos secundarios.                                                                                                      |
| E \_ OUTOFMEMORY          | El método no pudo asignar la memoria necesaria para completar una operación fundamental para su éxito.                                                                                                                                                                                                                                                                                        |
| E \_ FAIL                 | Se produjo un error desconocido o genérico.                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a>Valores devueltos adicionales

A continuación se muestran los valores devueltos que los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pueden devolver. Estos valores devueltos no son tan comunes como los anteriores, pero debe tenerlo en cuenta.



|                        |                                                                                      |
|------------------------|--------------------------------------------------------------------------------------|
| E \_ ACCESSDENIED        | Se devuelve cuando se llama a get \_ accValue para obtener el valor de un control de contraseña. |
| DISP \_ E ( \_ excepción)     |                                                                                      |
| CO \_ E \_ OBJNOTCONNECTED |                                                                                      |



 

 

 




