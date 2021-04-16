---
description: 'Antes de colocar los datos en el registro, una aplicación debe dividir los datos en dos categorías: datos específicos del equipo y datos específicos del usuario.'
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Categorías de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a3c89d23f713bb2ed08a7f7c53790e08055db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669981"
---
# <a name="categories-of-data"></a>Categorías de datos

Antes de colocar los datos en el registro, una aplicación debe dividir los datos en dos categorías: datos específicos del equipo y datos específicos del usuario. Al hacer esta distinción, una aplicación puede admitir varios usuarios y ubicar datos específicos del usuario en una red y usar esos datos en ubicaciones diferentes, lo que permite datos de Perfil de usuario independientes de la ubicación. (Un perfil de usuario es un conjunto de datos de configuración que se guarda para cada usuario).

Cuando se instala la aplicación, debe registrar los datos específicos del equipo en la clave **del \_ \_ equipo local HKEY** . En concreto, debe crear claves para el nombre de la compañía, el nombre del producto y el número de versión, como se muestra en el ejemplo siguiente:

**HKEY \_ \_ \\ Software \\ de máquina local**_MyCompany \\ \\ 1,0_

Si la aplicación admite COM, debe registrar esos datos en **\_ \_ \\ \\ las clases de software de máquina local HKEY**.

Una aplicación debe registrar datos específicos del usuario en la clave del **\_ \_ usuario actual HKEY** , tal como se muestra en el ejemplo siguiente:

**HKEY \_ \_ \\ Software \\ de usuario actual**, mi _\\ producto \\ 1,0_

 

 



