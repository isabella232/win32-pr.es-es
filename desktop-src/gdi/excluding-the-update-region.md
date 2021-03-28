---
description: La función ExcludeUpdateRgn excluye la región de actualización de la región de recorte para el contexto de dispositivo de pantalla.
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: Exclusión de la región de actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082360"
---
# <a name="excluding-the-update-region"></a>Exclusión de la región de actualización

La función [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) excluye la región de actualización de la región de recorte para el contexto de dispositivo de pantalla. Esta función es útil cuando se dibuja en una ventana distinta de cuando \_ se procesa un mensaje de pintura de WM. Impide dibujar en las áreas que se van a actualizar durante el siguiente mensaje de pintura de WM \_ .

 

 



