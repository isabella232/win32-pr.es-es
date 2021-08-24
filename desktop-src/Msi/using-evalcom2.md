---
description: 'Evalcom2.dll se puede usar para implementar operaciones de validación para los paquetes de instalación y los módulos de combinación mediante evaluadores de coherencia internos: TIC.'
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Uso de Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f89ba0215e697cb03111daa80510e6ba6c677c2e74f31e74b5640340d2d0d9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527131"
---
# <a name="using-evalcom2"></a>Uso de Evalcom2

Evalcom2.dll se puede usar para implementar operaciones de validación para paquetes de instalación y módulos de combinación mediante evaluadores de coherencia [internos: ICE](internal-consistency-evaluators-ices.md). El objeto principal implementa interfaces para programas de C/C++.

El objeto principal también implementa interfaces [Evalcom2](evalcom2-interfaces.md) para programas de C/C++. El CLSID necesario para obtener la interfaz de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) es {6E5E1910-8053-4660-B795-6B612E29BC58}. EL REFIID es {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.

Puede usar el procedimiento siguiente para implementar operaciones de validación.

**Para implementar operaciones de validación**

1.  Inicialice COM en el subproceso que realiza la llamada [**mediante CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).
2.  Obtenga el puntero a la [**interfaz IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) mediante [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).
3.  Abra el paquete de instalación o el módulo merge mediante el [**método OpenDatabase.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase)
4.  Abra el archivo de evaluación mediante el [**método OpenCUB.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub)
5.  Establezca la función de devolución de llamada de presentación mediante el [**método SetDisplay.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay)
6.  Establezca la función de devolución de llamada de estado mediante [**el método SetStatus.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus)
7.  Realice la validación mediante el [**método Validate.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate)
8.  Cierre el archivo .bina mediante el [**método CloseCUB.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub)
9.  Cierre la base de datos mediante [**el método CloseDatabase.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase)
10. Libere la [**interfaz IValidate.**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate)
11. Desinicializar COM mediante [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Evalcom2 Interfaces](evalcom2-interfaces.md)
</dt> <dt>

[Automatización de validación](validation-automation.md)
</dt> <dt>

[Funciones de devolución de llamada de validación](validation-callback-functions.md)
</dt> </dl>

 

 
