---
description: Implementa la interfaz IInkDesktopHost.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: InkDesktopHost (clase)
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: f422af645b3f5bc9431830c0ddab6f7321d09156b96fb6041104f684358bb9dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117884592"
---
# <a name="inkdesktophost-class"></a>InkDesktopHost (clase)

Implementa la [**interfaz IInkDesktopHost.**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)

Un [**objeto IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) permite la entrada de lápiz, el procesamiento y la representación mediante la creación de un subproceso de aplicación para hospedar un objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e insertarlo en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación.

## <a name="members"></a>Miembros

La **clase InkDesktopHost** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **InkDesktopHost también** tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La **clase InkDesktopHost** tiene estos métodos.

| Método | Descripción |
|---|---|
| [**CreateAndInitializeInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | Crea un [**objeto IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) en un subproceso de aplicación, lo conecta al árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación y establece el tamaño del objeto.<br/> |
| [**CreateInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | Crea un [**objeto IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) en un subproceso de aplicación.<br/> |
| [**QueueWorkItem**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | Agregue una operación de entrada de lápiz a una cola de trabajo para su ejecución en el **subproceso InkDesktopHost.**<br/> |

## <a name="creationaccess-functions"></a>Funciones de \\ acceso de creación

Llame a [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con el identificador de clase <strong>InkDesktopHost</strong> para recuperar una referencia al objeto .

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&_spInkHost));
```

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|---|---|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/> |
| Header<br/>                   | <dl> <dt>InkPresenterDesktop.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>InkPresenterDesktop.idl</dt> </dl> |
| IID<br/>                      | IID IInkDesktopHost se define como \_ 4ce7d875-a981-4140-a1ff-ad93258e8d59<br/> |

## <a name="related-topics"></a>Temas relacionados

[Clases de presentador de lápiz,](ink-presenter-classes.md) [interacciones de](/windows/uwp/design/input/pen-and-stylus-interactions)lápiz y [lápiz,](/samples/microsoft/windows-universal-samples/inkanalysis/)ejemplo de análisis de lápiz, ejemplo de entrada manuscrita [simple,](/samples/microsoft/windows-universal-samples/simpleink/) [ejemplo de entrada manuscrita compleja](/samples/microsoft/windows-universal-samples/complexink/)
