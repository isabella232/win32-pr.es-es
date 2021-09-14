---
description: En esta sección se describen las interfaces IMM.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Interfaces del Administrador de métodos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063096"
---
# <a name="input-method-manager-interfaces"></a>Interfaces del Administrador de métodos de entrada

En esta sección se describen las interfaces IMM.



| Interfaz                                                            | Descripción                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFECommon**](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | Proporciona servicios relacionados con IME que son comunes para distintos lenguajes.                                                                         |
| [**IFEDictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | Permite a los clientes acceder a un diccionario de usuarios de Microsoft IME.                                                                                      |
| [**IFELanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | Proporciona servicios de procesamiento de lenguaje mediante el IME de Microsoft.                                                                                 |
| [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | Inserta texto en aplicaciones de IMEPadApplets que implementan la [**interfaz IImePadApplet.**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                                 |
| [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | Introduce cadenas en las aplicaciones a través de [**la interfaz de IImePad.**](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                                                     |
| [**IImePlugInDictDictionaryList**](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | Proporciona acceso a la lista de diccionarios de complementos IME.                                                                                       |
| [**IImeSpecifyApplets**](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | Especifica los métodos a los que se llama desde el objeto de interfaz [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) para emular la [**interfaz IImePadApplet.**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) |



 

 

 



