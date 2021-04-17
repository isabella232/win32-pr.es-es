---
description: Las siguientes funciones se usan con el administrador de protección de salida (OPM).
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: Funciones de OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715532"
---
# <a name="opm-functions"></a>Funciones de OPM

Las siguientes funciones se usan con el [Administrador de protección de salida](output-protection-manager.md) (OPM).



| Función                                                                                             | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**OPMGetVideoOutputForTarget**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | Devuelve un objeto de salida de vídeo para el destino de VidPN en el adaptador especificado.                                                          |
| [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | Crea un objeto de administrador de protección de salida (OPM) para cada monitor físico que está asociado a un identificador de **HMONITOR** determinado. |
| [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | Crea un objeto OPM para cada monitor físico que está asociado a un dispositivo Direct3D determinado.                                 |



 

OPM usa las siguientes funciones para tener acceso a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a estas funciones.

-   [**ConfigureOPMProtectedOutput**](configureopmprotectedoutput.md)
-   [**CreateOPMProtectedOutputs**](createopmprotectedoutputs.md)
-   [**DestroyOPMProtectedOutput**](destroyopmprotectedoutput.md)
-   [**GetCertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [**GetCertificateSize**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [**GetCOPPCompatibleOPMInformation**](getcoppcompatibleopminformation.md)
-   [**GetOPMInformation**](getopminformation.md)
-   [**GetOPMRandomNumber**](getopmrandomnumber.md)
-   [**GetSuggestedOPMProtectedOutputArraySize**](getsuggestedopmprotectedoutputarraysize.md)
-   [**SetOPMSigningKeyAndSequenceNumbers**](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación de OPM](opm-programming-reference.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> </dl>

 

 



