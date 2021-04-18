---
description: Implementa la interfaz IInkDesktopHost.
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: Clase InkDesktopHost
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
ms.openlocfilehash: d5dac80a4ee09bb4b78a4d61ca0efa74e99babb9
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/12/2021
ms.locfileid: "105721319"
---
# <a name="inkdesktophost-class"></a>Clase InkDesktopHost

Implementa la interfaz [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) .

Un objeto [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) habilita la entrada de lápiz, el procesamiento y la representación a través de la creación de un subproceso de aplicación para hospedar un objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) e insertarlo en el árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación.

## <a name="members"></a>Miembros

La clase **InkDesktopHost** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **InkDesktopHost** también tiene estos tipos de miembros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **InkDesktopHost** tiene estos métodos.

| Método | Descripción |
|---|---|
| [**CreateAndInitializeInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | Crea un objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) en un subproceso de aplicación, lo conecta al árbol visual [DirectComposition](../directcomp/directcomposition-portal.md) de la aplicación y establece el tamaño del objeto.<br/> |
| [**CreateInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | Crea un objeto [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) en un subproceso de aplicación.<br/> |
| [**QueueWorkItem**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | Agregue una operación de entrada manuscrita a una cola de trabajo para su ejecución en el subproceso **InkDesktopHost** .<br/> |

## <a name="creationaccess-functions"></a>Funciones de acceso de creación \\

Llame a [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con el identificador de clase <strong>InkDesktopHost</strong> para recuperar una referencia al objeto.

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&amp;_spInkHost));
```

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|---|---|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/> |
| Encabezado<br/>                   | <dl> <dt>InkPresenterDesktop. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>InkPresenterDesktop. idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkDesktopHost se define como 4ce7d875-a981-4140-a1ff-ad93258e8d59<br/> |

## <a name="related-topics"></a>Temas relacionados

[Clases de presentador de tinta](ink-presenter-classes.md), [interacciones de lápiz y lápiz](/windows/uwp/design/input/pen-and-stylus-interactions), [ejemplo de análisis de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), ejemplo de tinta [simple](/samples/microsoft/windows-universal-samples/simpleink/), [ejemplo de tinta compleja](/samples/microsoft/windows-universal-samples/complexink/)
