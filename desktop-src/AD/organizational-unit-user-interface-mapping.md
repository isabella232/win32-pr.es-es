---
title: Asignación de la interfaz de usuario de unidades organizativas
description: En este tema se describen las hojas de propiedades de los objetos de la unidad organizativa (OU) en el complemento usuarios y equipos de Active Directory.
ms.assetid: 105c0f01-55d5-4dc2-887e-5e204ba82c4c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b8b08014d141c2182f47a5e3a40ebb9a18004ba
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904483"
---
# <a name="organizational-unit-user-interface-mapping"></a>Asignación de la interfaz de usuario de unidades organizativas

En este tema se describen las hojas de propiedades de los objetos de la unidad organizativa (OU) en el complemento usuarios y equipos de Active Directory.

## <a name="general-property-sheet"></a>Hoja de propiedades general

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **General** .



| Etiqueta de la interfaz de usuario        | Atributo en Active Directory Domain Services |
|-----------------|-----------------------------------------------|
| Descripción     | [**Descripción**](/windows/desktop/ADSchema/a-description)     |
| Calle          | [**Dirección postal**](/windows/desktop/ADSchema/a-street)       |
| City (Ciudad)            | [**Localidad: nombre**](/windows/desktop/ADSchema/a-l)             |
| Estado o provincia  | [**Nombre de estado o provincia**](/windows/desktop/ADSchema/a-st)   |
| Código postal | [**Código postal**](/windows/desktop/ADSchema/a-postalcode)      |
| País/región  | [**Nombre del país**](/windows/desktop/ADSchema/a-c)              |



 

## <a name="managed-by-property-sheet"></a>Administrado por hoja de propiedades

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la hoja de propiedades **administrado por** .



| Etiqueta de la interfaz de usuario         | Atributo en Active Directory Domain Services                                                                                   |
|------------------|---------------------------------------------------------------------------------------------------------------------------------|
| Nombre             | [**Administrado: por**](/windows/desktop/ADSchema/a-managedby)                                                                                          |
| Office           | El atributo [**Physical-Delivery-Office-Name**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) de la cuenta identificada por **Name**. |
| Calle           | El atributo [**calle-dirección**](/windows/desktop/ADSchema/a-street) de la cuenta identificada por **nombre**.                                    |
| City (Ciudad)             | El atributo [**localidad-nombre**](/windows/desktop/ADSchema/a-l) de la cuenta identificada por **nombre**.                                          |
| Estado o provincia   | El atributo [**State-or-provincia-Name**](/windows/desktop/ADSchema/a-st) de la cuenta identificada por **Name**.                                |
| País/región   | El atributo [**Country-name**](/windows/desktop/ADSchema/a-c) de la cuenta identificada por **Name**.                                           |
| Número de teléfono | El atributo de [**número de teléfono**](/windows/desktop/ADSchema/a-telephonenumber) de la cuenta identificada por **nombre**.                         |
| Número de fax       | El atributo [**facsímil-Phone-Number**](/windows/desktop/ADSchema/a-facsimiletelephonenumber) de la cuenta identificada por **Name**.      |



 

 

 