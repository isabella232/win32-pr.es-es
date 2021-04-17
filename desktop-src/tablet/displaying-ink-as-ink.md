---
description: El comportamiento predeterminado del control InkEdit es reconocer y convertir la entrada manuscrita en texto después de que haya expirado un breve tiempo de espera.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Mostrar la entrada de lápiz como entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aca1d6a1a4700d996d65a9cfd7d62e6b27e1c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697566"
---
# <a name="displaying-ink-as-ink"></a><span data-ttu-id="fc913-103">Mostrar la entrada de lápiz como entrada de lápiz</span><span class="sxs-lookup"><span data-stu-id="fc913-103">Displaying Ink as Ink</span></span>

<span data-ttu-id="fc913-104">El comportamiento predeterminado del control [InkEdit](inkedit-control-reference.md) es reconocer y convertir la entrada manuscrita en texto después de que haya expirado un breve tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="fc913-104">The default behavior for the [InkEdit](inkedit-control-reference.md) control is to recognize and convert ink into text after a brief timeout has expired.</span></span> <span data-ttu-id="fc913-105">Dado que el control es una superclase de [RichEdit](../controls/rich-edit-controls.md), también es posible incrustar y mostrar la entrada de lápiz en el control.</span><span class="sxs-lookup"><span data-stu-id="fc913-105">Because the control is a superclass of [RichEdit](../controls/rich-edit-controls.md), it is also possible to embed and display ink within the control.</span></span> <span data-ttu-id="fc913-106">Cada palabra se inserta en el control como un objeto [**InkDisp**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="fc913-106">Each word is inserted into the control as an [**InkDisp**](inkdisp-class.md) object.</span></span> <span data-ttu-id="fc913-107">El objeto **InkDisp** contiene la tinta y sus alternativas de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="fc913-107">The **InkDisp** object contains the ink and its recognition alternates.</span></span>

<span data-ttu-id="fc913-108">Cuando se inserta, la tinta se escala hasta el tamaño de fuente actual y se aplican otras propiedades de ambiente, como cursiva o negrita.</span><span class="sxs-lookup"><span data-stu-id="fc913-108">When inserted, the ink is scaled to the current font size and other ambient properties, such as italics or bold, are applied.</span></span> <span data-ttu-id="fc913-109">Si el usuario decide editar el texto de un objeto [**InkDisp**](inkdisp-class.md) , primero debe convertir la tinta en texto.</span><span class="sxs-lookup"><span data-stu-id="fc913-109">If the user chooses to edit the text of an [**InkDisp**](inkdisp-class.md) object, he or she must first convert the ink to text.</span></span>

> [!Note]  
> <span data-ttu-id="fc913-110">Todos los datos alternativos de reconocimiento y de entrada de lápiz se pierden durante la conversión.</span><span class="sxs-lookup"><span data-stu-id="fc913-110">All ink and recognition alternate data is lost during the conversion.</span></span>

 

<span data-ttu-id="fc913-111">Esta característica solo está disponible en equipos que ejecutan Microsoft Windows XP Tablet PC Edition, Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="fc913-111">This feature is available only on computers that run Microsoft Windows XP Tablet PC Edition, Windows Vista, or later.</span></span>

 

 
