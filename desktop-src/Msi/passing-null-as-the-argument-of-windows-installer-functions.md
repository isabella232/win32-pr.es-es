---
description: 'Windows Installer funciones que devuelven datos en un usuario proporcionado: no se debe llamar a la ubicación de memoria con NULL como valor del puntero.'
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Pasar null a Windows Installer funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb09ceb3982695792614a3c226af9ab276aa3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652524"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a>Pasar null como argumento de funciones de Windows Installer

Windows Installer funciones que devuelven datos en un usuario proporcionado: no se debe llamar a la ubicación de memoria con NULL como valor del puntero. Estas funciones devuelven una cadena o devuelven datos como punteros enteros, pero devuelven valores incoherentes al pasar null como valor para el argumento de salida.

No pase NULL como el valor del argumento Output para cualquiera de las siguientes funciones:

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

 

 



