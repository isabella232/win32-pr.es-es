---
description: Las siguientes funciones se usan con Output Protection Manager (OPM).
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: Funciones de OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de880584716c5caac94c93e48dd89ded481c14e1c7a08be3e23ac334e1c8bfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058769"
---
# <a name="opm-functions"></a>Funciones de OPM

Las siguientes funciones se usan con [Output Protection Manager](output-protection-manager.md) (OPM).



| Función                                                                                             | Descripción                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**OPMGetVideoOutputForTarget**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | Devuelve un objeto de salida de vídeo para el destino VidPN en el adaptador especificado.                                                          |
| [**OPMGetVideoOutputsFromHMONITOR**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | Crea un objeto de Administrador de protección de salida (OPM) para cada monitor físico asociado a un identificador **HMONITOR** determinado. |
| [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | Crea un objeto OPM para cada monitor físico asociado a un dispositivo Direct3D determinado.                                 |



 

OPM usa las siguientes funciones para acceder a la funcionalidad del controlador de pantalla. Las aplicaciones no deben llamar a estas funciones.

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

 

 



