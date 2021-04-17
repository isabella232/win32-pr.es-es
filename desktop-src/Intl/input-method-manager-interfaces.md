---
description: En esta sección se describen las interfaces de IMM.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Interfaces del administrador de métodos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687614"
---
# <a name="input-method-manager-interfaces"></a>Interfaces del administrador de métodos de entrada

En esta sección se describen las interfaces de IMM.



| Interfaz                                                            | Descripción                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFECommon**](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | Proporciona servicios relacionados con el IME que son comunes para distintos idiomas.                                                                         |
| [**IFEDictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | Permite a los clientes tener acceso a un diccionario de usuario IME de Microsoft.                                                                                      |
| [**IFELanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | Proporciona servicios de procesamiento de lenguajes mediante Microsoft IME.                                                                                 |
| [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | Inserta texto en las aplicaciones de IMEPadApplets que implementan la interfaz [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .                                 |
| [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | Introduce cadenas en aplicaciones a través de la interfaz [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) .                                                                     |
| [**IImePlugInDictDictionaryList**](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | Proporciona acceso a la lista de diccionarios de complemento IME.                                                                                       |
| [**IImeSpecifyApplets**](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | Especifica los métodos llamados desde el objeto de interfaz [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) para emular la interfaz [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) . |



 

 

 



