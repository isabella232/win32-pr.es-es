---
title: Comunicación de cliente NAP y componente del lado servidor
description: Comunicación de cliente NAP y componente del lado servidor
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3c390aa8bdc8cc80eec8834dd1c250d523737d63963b4b9370877ffa46329
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799085"
---
# <a name="nap-client-and-server-side-component-communication"></a>Comunicación de cliente NAP y componente del lado servidor

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

El componente del Agente NAP puede comunicarse con el componente servidor de administración de NAP a través del proceso siguiente:

1.  El agente NAP pasa el SSoH a NAP EC.
2.  Nap EC pasa el SSoH a NAP ES.
3.  NAP ES pasa el SSoH al servicio Servidor de directivas de red (NPS).
4.  El servicio NPS pasa el SSoH al servidor de administración de NAP.

Un SHA puede comunicarse con su SHV correspondiente a través del proceso siguiente:

1.  Sha pasa su SoH al agente NAP.
2.  El agente NAP pasa el SoH, contenido en el SSoH, a nap EC.
3.  Nap EC pasa el SoH a NAP ES.
4.  NAP ES pasa el SoH al servidor de administración de NAP.
5.  El servidor de administración de NAP pasa el SoH al SHV.

En la ilustración siguiente se muestra el proceso de comunicación entre los componentes de cliente NAP y los componentes del lado servidor NAP.

![arquitectura de la comunicación de cliente a servidor en la plataforma nap](images/nap-client-to-server-comm.png)

El servidor de administración de NAP puede comunicarse con el agente NAP a través del siguiente proceso:

1.  El servidor de administración de NAP pasa los SOHR al servicio NPS.
2.  El servicio NPS pasa el SSoHR a NAP ES.
3.  NAP ES pasa el SSoHR a NAP EC.
4.  Nap EC pasa el SSoHR al agente NAP.

La SHV puede comunicarse con su SHA correspondiente a través del proceso siguiente:

1.  La SHV pasa su SoHR al servidor de administración nap.
2.  El servidor de administración nap pasa el SoHR al servicio NPS.
3.  El servicio NPS pasa el SoHR, contenido dentro de SSoHR, a nap ES.
4.  NAP ES pasa el SoHR a NAP EC.
5.  NAP EC pasa el SoHR al agente NAP.
6.  El agente NAP pasa el SoHR al SHA.

En la ilustración siguiente se muestra el proceso de comunicación de los componentes del lado servidor NAP a los componentes de cliente NAP.

![arquitectura de la comunicación de servidor a cliente en la plataforma nap](images/nap-server-to-client-comm.png)

 

 




