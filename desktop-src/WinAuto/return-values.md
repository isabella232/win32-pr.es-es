---
title: Valores devueltos (Windows de accesibilidad)
description: En este tema se describen los valores devueltos más comunes y otros valores devueltos que puede ver con menos frecuencia.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71595f7a21d932ee961f9fa5f2a9443cf4d63e38de42f3d5b8c89fa8e9f84e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122065"
---
# <a name="return-values-windows-accessibility-features"></a>Valores devueltos (Windows de accesibilidad)

En este tema se describen los valores devueltos más comunes y otros valores devueltos que puede ver con menos frecuencia.

## <a name="common-return-values"></a>Valores devueltos comunes

Los [**métodos IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) devuelven uno de los siguientes valores, definidos en winerror.h, u otro código de error estándar del Modelo de objetos componentes (COM):



|   Value                      |   Descripción                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK                   | El método se ha llevado a cabo de forma correcta.                                                                                                                                                                                                                                                                                                                                                                     |
| S \_ FALSE                | El método se ha instalado correctamente en parte. Esto sucede cuando el método se realiza correctamente, pero la información solicitada no está disponible. Por ejemplo, Microsoft Active Accessibility devuelve S FALSE si llama \_ a [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) para recuperar un objeto secundario en un punto determinado y el punto especificado no está dentro del objeto o del elemento secundario del objeto. |
| DISP \_ E \_ MEMBERNOTFOUND | El objeto no admite la propiedad o la acción solicitadas. Por ejemplo, un botón de inserción devuelve este valor si solicita su [propiedad Value](value-property.md), porque no tiene una propiedad Value.                                                                                                                                                                           |
| E \_ NOTIMPL              | El método no está implementado. Este valor se produce cuando un cliente llama a un método que aún no se admite en ese sistema operativo.                                                                                                                                                                                                                                                         |
| E \_ INVALIDARG           | Uno o varios argumentos no eran válidos. Este error se produce cuando el autor de la llamada intenta identificar un objeto secundario mediante un identificador que el servidor no reconoce. Este error también se produce cuando un cliente intenta identificar un objeto secundario dentro de un objeto que no tiene elementos secundarios.                                                                                                      |
| E \_ OUTOFMEMORY          | El método no pudo asignar la memoria necesaria para completar una operación crucial para su éxito.                                                                                                                                                                                                                                                                                        |
| E \_ FAIL                 | Se produjo un error desconocido o genérico.                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a>Valores devueltos adicionales

Los siguientes son valores devueltos que [**los métodos IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) podrían devolver. Estos valores devueltos no son tan comunes como los anteriores, pero debe tener en cuenta estos valores.



|    Value                    |    Descripción                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| E \_ ACCESSDENIED        | Esto se devuelve cuando se llama a get \_ accValue para obtener el valor de un control de contraseña. |
| EXCEPCIÓN \_ DISP E \_     |                                                                                      |
| CO \_ E \_ OBJNOTCONNECTED |                                                                                      |



 

 

 




