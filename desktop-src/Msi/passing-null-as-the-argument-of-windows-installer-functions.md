---
description: Windows No se debe llamar a las funciones del instalador que devuelven datos en una ubicación de memoria proporcionada por el usuario con null como valor para el puntero.
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Pasar null a Windows Installer Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6964716479d7e64cc9aa70d7e49acc8fe78dd3343298826e011f6d72b4df1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627668"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a>Pasar null como argumento de las Windows instalador

Windows No se debe llamar a las funciones del instalador que devuelven datos en una ubicación de memoria proporcionada por el usuario con null como valor para el puntero. Estas funciones devuelven una cadena o devuelven datos como punteros enteros, pero devuelven valores incoherentes al pasar null como valor para el argumento de salida.

No pase Null como valor del argumento de salida para ninguna de las funciones siguientes:

[**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[**MsiGetSourcePath**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[**MsiGetFeatureCost**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[**MsiGetFeatureValidStates**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



