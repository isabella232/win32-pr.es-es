---
description: 'Antes de colocar datos en el Registro, una aplicación debe dividir los datos en dos categorías: datos específicos del equipo y datos específicos del usuario.'
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Categorías de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a3c89d23f713bb2ed08a7f7c53790e08055db
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124371875"
---
# <a name="categories-of-data"></a>Categorías de datos

Antes de colocar datos en el Registro, una aplicación debe dividir los datos en dos categorías: datos específicos del equipo y datos específicos del usuario. Al hacer esta distinción, una aplicación puede admitir varios usuarios y, sin embargo, localizar datos específicos del usuario a través de una red y usarlos en ubicaciones diferentes, lo que permite datos de perfil de usuario independientes de la ubicación. (Un perfil de usuario es un conjunto de datos de configuración guardados para cada usuario).

Cuando se instala la aplicación, debe registrar los datos específicos del equipo en la **clave HKEY \_ LOCAL \_ MACHINE.** En concreto, debe crear claves para el nombre de la empresa, el nombre del producto y el número de versión, como se muestra en el ejemplo siguiente:

**HKEY \_ LOCAL \_ MACHINE \\ \\ Software**_MyCompany \\ MyProduct \\ 1.0_

Si la aplicación admite COM, debe registrar los datos en clases de **software HKEY \_ LOCAL \_ \\ \\ MACHINE**.

Una aplicación debe registrar datos específicos del usuario en la **clave HKEY \_ CURRENT \_ USER,** como se muestra en el ejemplo siguiente:

**HKEY \_ CURRENT \_ USER \\ \\ Software**_MyCompany \\ MyProduct \\ 1.0_

 

 



