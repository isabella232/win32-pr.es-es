---
title: Devolver información de error
description: Devolver información de error
ms.assetid: 4206f2e5-db01-458c-93cb-10c5cd4a4536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 303db82dc220d09d4db7f52bf4c04ad1e5ca691f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421439"
---
# <a name="returning-error-information"></a>Devolver información de error

Mediante las interfaces y funciones de control de errores de COM, puede devolver información de error realizando los pasos siguientes:

1.  Implemente la interfaz [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo) .
2.  Para crear una instancia del objeto de error genérico, llame a la función [**CreateErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo) .
3.  Para establecer su contenido, use los métodos [**ICreateErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo) .
4.  Para asociar el objeto de error al subproceso lógico actual, llame a la función [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) .

Las interfaces de control de errores crean y administran un objeto de error, que proporciona información sobre el error. El objeto de error no es el mismo que el objeto que encontró el error. Es un objeto independiente asociado al subproceso de ejecución actual.

 

 