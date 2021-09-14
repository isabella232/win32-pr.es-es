---
title: Control de errores COM en Java y Visual Basic
description: Control de errores COM en Java y Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11c55c1c2414c69ff9398845858baadebd58cbf9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060946"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a>Control de errores COM en Java y Visual Basic

Hay tres interfaces y tres funciones que se pueden usar en COM para proporcionar control de errores al programar en Java o Microsoft Visual Basic. En Java y Visual Basic, la llamada al método no devuelve **un valor HRESULT** como valor devuelto. En su lugar, estos lenguajes usan las interfaces y funciones COM para obtener valores **HRESULT** y controlar errores o excepciones. (Las excepciones son eventos más allá del control del programa, como problemas de archivos o parámetros no válidos).

Las tres interfaces que proporcionan compatibilidad con **HRESULT** se enumeran y describen brevemente en la tabla siguiente.



|  Interfaz                                                                        |  Descripción                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | Establece la información de error.<br/>                                                                                   |
| [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | Devuelve información de un objeto de error.<br/>                                                                 |
| [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | Identifica el objeto como compatible con la [**interfaz IErrorInfo.**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/> |



 

Las tres funciones que proporcionan compatibilidad con **HRESULT** se enumeran y describen brevemente en la tabla siguiente.



|    Interfaz       |       Descripción       |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | Crea una instancia de un objeto de error genérico.<br/>                                                                                                            |
| [**GetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | Obtiene el puntero de información de error establecido por la llamada anterior a [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) en el subproceso lógico actual.<br/> |
| [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | Establece el objeto de información de error para el subproceso de ejecución actual.<br/>                                                                                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Control de errores en COM](error-handling-in-com.md)
</dt> </dl>

 

