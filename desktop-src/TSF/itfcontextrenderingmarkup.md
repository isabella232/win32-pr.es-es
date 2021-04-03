---
title: Interfaz ITfContextRenderingMarkup
description: La interfaz ITfContextRenderingMarkup se implementa mediante el administrador de TSF y la usan las aplicaciones. Esta interfaz se puede recuperar mediante IQueryInterface del objeto ITfContext. Esta interfaz ayuda a la aplicación a enumerar la información de representación.
ms.assetid: 733d2db2-f9e9-4b78-af13-adc03825bf2b
keywords:
- ITfContextRenderingMarkup interface Text Services Framework
- ITfContextRenderingMarkup interface Text Services Framework, descrito
topic_type:
- apiref
api_name:
- ITfContextRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b71e977665a4b3a6e817ef782ee558064e0986a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904691"
---
# <a name="itfcontextrenderingmarkup-interface"></a>Interfaz ITfContextRenderingMarkup

La interfaz **ITfContextRenderingMarkup** se implementa mediante el administrador de TSF y la usan las aplicaciones. Esta interfaz se puede recuperar mediante IQueryInterface del objeto [ITfContext](/windows/desktop/api/Msctf/nn-msctf-itfcontext) . Esta interfaz ayuda a la aplicación a enumerar la información de representación.



| Métodos ITfContextRenderingMarkup                                                | Descripción                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md)           | Recupera un enumerador de los marcas de representación para el intervalo especificado. |
| [FindNextRenderingMarkup](itfcontextrenderingmarkup-findnextrenderingmarkup.md) | Esta función no está implementada. Siempre devuelve E \_ NOTIMPL.       |



 

## <a name="members"></a>Miembros

La interfaz **ITfContextRenderingMarkup** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , pero no tiene miembros adicionales.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Esta interfaz no está actualmente en los archivos de encabezado públicos. Para usar esta API, debe compilar MIDL en el [prototipo](prototypes.md).

 

 

 